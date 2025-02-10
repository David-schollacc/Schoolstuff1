import pygame

pygame.init()

#Farben die ich Maybe benutzen will BLACK = (0, 0, 0) WHITE = (255, 255, 255) RED = (255, 0, 0)

#Fenster Größe => beinflusst nicht die Größe wie gedacht ist aber notwendig screen = pygame.display.set_mode((640, 480))

#Fenster Name pygame.display.set_caption("Tic-Tac-Toe")

GameOn = True

SpielerposY = 300 Spielfigure = 0

#Bildschirm aktualisieren clock = pygame.time.Clock()

#versuchen dass das game an bleibt while GameOn: for event in pygame.event.get(): if event.type == pygame.QUIT: GameOn = False elif event.type == pygame.KEYDOWN:

        #Player 1
        if event.key == pygame.K_RIGHT:
            print("Spieler 1: Rechts")
        elif event.key == pygame.K_LEFT:
            print("Spieler 1: Links")
        elif event.key == pygame.K_UP:
            print("Spieler 1: Hoch")
        elif event.key == pygame.K_DOWN:
            print("Spieler 1: Runter")
        elif event.key == pygame.K_SPACE:
            print("Spieler 1: Leertaste")
        #Player 2
        elif event.key == pygame.K_w:
            print("Spieler 2: Hoch")
        elif event.key == pygame.K_a:
            print("Spieler 2: Links")
        elif event.key == pygame.K_s:
            print("Spieler 2: Runter")
        elif event.key == pygame.K_d:
            print("Spieler 2: Rechts")
    elif event.type == pygame.MOUSEBUTTONDOWN:
        print("Spieler 2: Maus")
#Fenster schließen screen.fill(WHITE)

#Fenster aktualisieren pygame.display.flip()

#FPS clock.tick(60)

pygame.quit()
