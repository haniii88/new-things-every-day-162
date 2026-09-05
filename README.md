function dailyLog162() {
  const expenses = [
    { name: "Food", amount: 18 },
    { name: "Transport", amount: 12 },
    { name: "Books", amount: 25 },
    { name: "Coffee", amount: 6 },
    { name: "Snacks", amount: 9 }
  ];

  const total = expenses.reduce((sum, item) => sum + item.amount, 0);
  const largest = expenses.reduce((max, item) =>
    item.amount > max.amount ? item : max
  );

  const report = {
    date: new Date().toISOString().split("T")[0],
    totalExpenses: total,
    largestExpense: largest.name,
    largestAmount: largest.amount
  };

  console.log("Daily Expense Report:", report);
}

dailyLog162();
