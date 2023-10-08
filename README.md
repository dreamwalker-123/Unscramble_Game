Unscramble app
=================================

Single player game app that displays scrambled words. To play the game, player has to make a
word using all the letters in the displayed scrambled word.
This code demonstrates the Android Architecture component- ViewModel and StateFlow.


what we have here:
1) private val _uiState = MutableStateFlow(GameUiState())
   val uiState: StateFlow<GameUiState> = _uiState.asStateFlow()
2) var userGuess by mutableStateOf("")
3) _uiState.update { currentState ->
       currentState.copy(isGuessedWordWrong = true)
   }
4) val gameUiState by gameViewModel.uiState.collectAsState()
5) val activity = (LocalContext.current as Activity)
