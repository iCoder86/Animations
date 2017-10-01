# MenuAnimation

<img src="https://github.com/iCoder86/MenuAnimation/blob/master/Animation/Animation/MenuAnimation.gif" title="made at imgflip.com"/>

    @IBAction func toggleMenuButton(_ sender:UIButton?) {
        if btnMenu.tag == 0 {
            self.btnMenu.tag = 1
            UIView.animate(withDuration: 0.3, animations: {
                self.btnShuffel.center = self.btnMenu.center
                self.btnFavorite.center = self.btnMenu.center
                self.btnRepeat.center = self.btnMenu.center
                
                self.btnShuffel.alpha = 0
                self.btnFavorite.alpha = 0
                self.btnRepeat.alpha = 0
            })
        }
        else {
            self.btnMenu.tag = 0
            UIView.animate(withDuration: 0.3, animations: {
                self.btnShuffel.center = self.btnShuffelPosition
                self.btnFavorite.center = self.btnFavoritePosition
                self.btnRepeat.center = self.btnRepeatPosition
                
                self.btnShuffel.alpha = 1
                self.btnFavorite.alpha = 1
                self.btnRepeat.alpha = 1
            })
        }
    }
