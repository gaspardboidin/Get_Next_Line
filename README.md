***🇺🇸 English Version - get_next_line***


***📝 Description***

This project was developed as part of the 42 School common core curriculum.
The goal is to implement a function that reads and returns one line at a time from a file descriptor, while ensuring optimized memory management.


***🚀 Features***

✅ Line-by-line reading: Reads and returns each line from a file until EOF.

✅ Optimized memory management: Keeps only necessary data in memory.

✅ Dynamic buffer usage: Works with a customizable BUFFER_SIZE macro, set at compilation.

✅ Compatibility: Can read from a file, stdin, or any file descriptor.


***📌 Compilation***

gcc -Wall -Wextra -Werror -D BUFFER_SIZE=42 get_next_line.c get_next_line_utils.c

(The BUFFER_SIZE can be defined during compilation. If not specified, a default behavior is applied.)


***📂 Project Structure***

📌 get_next_line.c → Implements the main function.

📌 get_next_line_utils.c → Includes utility functions (memory handling, string operations, etc.).

📌 get_next_line.h → Contains function prototypes and necessary definitions.


***🎯 Skills Developed***

✔️ Advanced file descriptor handling.

✔️ Dynamic memory management (malloc, free, memory leak prevention).

✔️ Buffer optimization to minimize system calls.

✔️ Experience with the strict 42 coding standard.


***📌 Usage - C Example***
```
#include <fcntl.h>
#include <stdio.h>
#include "get_next_line.h"

int main(void)
{
    int fd = open("test.txt", O_RDONLY);
    char *line;

    while ((line = get_next_line(fd)))
    {
        printf("%s\n", line);
        free(line);
    }
    close(fd);
    return (0);
}
```


***📜 License***

This project is under the *MIT License* – you are free to use, modify, and distribute it.


---------------------------------------------------------------------------------------------------


🇫🇷 Version Française - get_next_line

📝 Description

Ce projet a été réalisé dans le cadre du tronc commun de l'École 42.
Il a pour objectif d’implémenter une fonction permettant de lire et retourner une ligne à la fois depuis un fichier, tout en respectant les contraintes de gestion de mémoire et d’optimisation.

🚀 Fonctionnalités

✅ Lecture ligne par ligne : La fonction renvoie chaque ligne d'un fichier jusqu'à la fin.
✅ Gestion optimisée de la mémoire : Stocke uniquement les données nécessaires.
✅ Buffer dynamique : Fonctionne avec une macro BUFFER_SIZE, ajustable à la compilation.
✅ Compatibilité : Peut lire depuis un fichier, stdin, ou tout descripteur de fichier.

📌 Compilation
sh
gcc -Wall -Wextra -Werror -D BUFFER_SIZE=42 get_next_line.c get_next_line_utils.c

(Le BUFFER_SIZE peut être défini à la compilation. S’il n’est pas spécifié, un comportement par défaut est appliqué.)


📂 Structure du projet

📌 get_next_line.c → Implémente la fonction principale.
📌 get_next_line_utils.c → Contient les fonctions utilitaires (gestion de mémoire, manipulation de chaînes, etc.).
📌 get_next_line.h → Définitions et prototypes nécessaires.

🎯 Compétences Développées

✔️ Gestion avancée des descripteurs de fichiers.
✔️ Gestion dynamique de la mémoire (malloc, free, prévention des fuites).
✔️ Optimisation des buffers pour minimiser les appels système.
✔️ Respect de la norme stricte de l'École 42.

📜 Licence

Ce projet est sous MIT License – vous êtes libre de l'utiliser, le modifier et le distribuer.


