Ce projet permet de générer du code **CadQuery** à partir d'une image d'objet mécanique 2D, grâce à un modèle deep learning entraîné sur la dataset [GenCAD](https://huggingface.co/datasets/CADCODER/GenCAD-Code).

## 🔧 Architecture

- **Encodeur image** : ViT (`google/vit-base-patch16-224-in21k`) pré-entraîné, figé
- **Projection** : couche `Linear(768 → 512)` pour adapter au décodeur
- **Décodeur** : `CodeT5-small` (pré-entraîné) qui génère le code CAD

L’image est encodée en un vecteur `CLS`, projetée dans l’espace de CodeT5, et insérée comme 1er token dans la séquence d’entrée.

## 📦 Données

- Dataset : `CADCODER/GenCAD-Code`
- Chaque exemple contient :
  - Une image 2D (PNG)
  - Le code CadQuery correspondant
