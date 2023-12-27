FullStack Development Assessment

1. Single correct answer question: What command is used to rewrite commit history and
maintain a linear project history by incorporating changes from one branch into another?
A) git merge
B) git rebase
C) git commit
D) git log
Ans: B) git rebase

2. Single correct answer question: To selectively apply a specific commit from one branch
to another, which Git command should be used?
A) git commit --cherry-pick
B) git revert
C) git branch
D) git apply
Ans.A) git commit --cherry-pick

3. Single correct answer question: Which Git command facilitates the creation of multiple
isolated working directories for the same repository?
A) git switch
B) git branch
C) git worktree
D) git clone
Ans.C) git worktree

4. Short answer question: You encounter a merge conflict while merging a featurebranch
into the main branch. How will you address it. Write the git commands in appropriate
order.
Ans.
step 1=> git fetch origin
step 2=> git checkout <branch_name>
step 3=> git merge <feature_branch>
step 4=> git status
step 5=> git add <files>
step 6=> git commit -m <branch_name>
step 7=> git push origin master

7. Short answer question: You have to design a card with React. Which of the two would
you design. Also write down your reasoning for your answer.
A) Either A or B
B) A only
C) B only
D) I do not know
Ans.C) B only Because used all the Css and react libraries

8. Single correct answer question: What is the name of the React Hook that lets a
component read the value of a context?
A) useProvider
B) useConsumer
C) useContext
D) useData
Ans.C) useContext

9. Multiple correct answer question: When selecting and using third-party UI component
libraries in a React project, what factors should be considered to maintain a consistent
and user-friendly design?
A) Assess the library's customization options
B) Evaluate community support and updates
C) Consider the library's impact on the overall bundle size
D) I do not know
Ans.
A) Assess the library's customization options
B) Evaluate community support and updates
C) Consider the library's impact on the overall bundle size

10. Multiple correct answer question: When optimizing the performance of a React
application, which strategies can help reduce the bundle size and improve load times?
A) Code splitting
B) Tree shaking
C) Minification
D) Inline all styles
E) I do not know
Ans.
A) Code splitting
B) Tree shaking
C) Minification

11. Multiple correct answer question: When incorporating internationalization (i18n) in a
React application, which practices contribute to a better user experience for users from
diverse linguistic backgrounds?
A) Use a library like react-intl for message translation
B) Store translatable strings in separate JSON files
C) Rely solely on browser-based language detection
D) Ensure text is not embedded in images for translation flexibility
E) I do not know
Ans.
A) Use a library like react-intl for message translation
B) Store translatable strings in separate JSON files
D) Ensure text is not embedded in images for translation flexibility

PROGRAMMING SOLVING 
5. Coding question: Click the below link and solve the problem. Submit the correct output
and code in a git repository link.

Answer: 

function hashAlgorithm(input) {
  let currentValue = 0;
  for (let i = 0; i < input.length; i++) {
    const charCode = input.charCodeAt(i);
    currentValue += charCode;
    currentValue *= 17;
    currentValue %= 256;
  }
  return currentValue;
}

function sumOfHashResults(sequence) {
  const steps = sequence.split(',');
  let totalSum = 0;

  steps.forEach(step => {
    const result = hashAlgorithm(step.replace(/\n/g, '').replace(/\s/g, ''));
    totalSum += result;
  });

  return totalSum;
}
const initializationSequence = "rn=1,cm-,qp=3,cm=2,qp-,pc=4,ot=9,ab=5,pc-,pc=6,ot=7";
const sum = sumOfHashResults(initializationSequence);
console.log("The sum of the results is:", sum);

6. Coding question: Go to the following link and solve the problem. Submit the correct
output and code in a git repository link.

Answer:

function calculateTotalLoad(grid) {
  const rows = grid.length;
  const cols = grid[0].length;

  let totalLoad = 0;

  const calculateLoad = (row, col) => {
    let load = 0;
    for (let r = row + 1; r < rows; r++) {
      if (grid[r][col] === '.') {
        load++;
      } else {
        break;
      }
    }
    return load;
  };

 for (let i = 0; i < rows; i++) {
    for (let j = 0; j < cols; j++) {
      if (grid[i][j] === 'O') {
        totalLoad += calculateLoad(i, j);
      }
    }
  }

  return totalLoad;
}

const inputGrid = [
  "O....#....",
  "O.OO#....#",
  ".....##...",
  "OO.#O....O",
  ".O.....O#.",
  "O.#..O.#.#",
  "..O..#O..O",
  ".......O..",
  "#....###..",
  "#OO..#...."
];

const totalLoad = calculateTotalLoad(inputGrid);
console.log("The total load on the north support beams is:", totalLoad);

