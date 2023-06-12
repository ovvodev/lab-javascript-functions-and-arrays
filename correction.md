great work!

for the second bonus, this is a mathematical concept called matrix multiplication, where you need to add the product of each row element from matrix 1 by each column element from matrix 2, here is a video explaining it: https://www.youtube.com/watch?v=2spTnAiQg4M, 
this would be a valid solution for example:

  const row = matrix.length - 1;
  const col = matrix[0].length - 1;

  let finalProduct = 0,
    maxProduct;

  for (let i = 0; i <= row; i++) {
    for (let j = 0; j <= col; j++) {
      if (i + 3 <= row) {
        maxProduct =
          matrix[i][j] * matrix[i + 1][j] * matrix[i + 2][j] * matrix[i + 3][j];
        if (maxProduct > finalProduct) finalProduct = maxProduct;
      }

      if (j + 3 <= col) {
        maxProduct =
          matrix[i][j] * matrix[i][j + 1] * matrix[i][j + 2] * matrix[i][j + 3];
        if (maxProduct > finalProduct) finalProduct = maxProduct;
      }
    }
  }
  return finalProduct;
 
