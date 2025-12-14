# Diagram Przepływu Aplikacji (Mermaid Flowchart)

Poniższy diagram przedstawia główną pętlę logiczną programu z użyciem Mermaid.

```mermaid
flowchart TD
    A([START]) --> B{Onboarding: Ustawienia};
    B --> C{Pętla: Menu Główne};
    C --> D[Lista Zadań];
    C --> E[Widok Kalendarza];
    D --> F[Utwórz / Edytuj Zadanie];
    F --> G[Zapisz Zadanie];
    G --> H{Przypisać do Kalendarza?};
    H --TAK--> E;
    H --NIE--> D;
    D --> I[Oznacz jako Ukończone];
    I --> J[Zaktualizuj Statystyki];
    J --> C;
    E --> C;
    C --> K([END]);