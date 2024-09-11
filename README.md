# chemical-reactionclass ChemicalReaction:
    def __init__(self, hydrogen, oxygen):
        self.hydrogen = hydrogen  # Number of H₂ molecules
        self.oxygen = oxygen      # Number of O₂ molecules

    def react(self):
        # Reaction: 2H₂ + O₂ -> 2H₂O
        # 2 H₂ molecules react with 1 O₂ molecule to form 2 H₂O molecules.
        while self.hydrogen >= 2 and self.oxygen >= 1:
            self.hydrogen -= 2
            self.oxygen -= 1
            print("Reaction occurred: 2 H₂ + 1 O₂ -> 2 H₂O")
        print(f"Remaining hydrogen: {self.hydrogen}, Remaining oxygen: {self.oxygen}")

# Example usage:
reaction = ChemicalReaction(hydrogen=6, oxygen=3)  # Starting with 6 H₂ and 3 O₂ molecules
reaction.react()
