# Jak zacząć swoją przygode z GP CTF
## To bardzo proste.
### Po prostu wejdź na [stronę z challangami](https://gpctf.cytr.us) wybierz jeden dla siebie i zacznij swoją przygode z hakingiem
# Docker
### Do niektórych challangy będziesz potrzebował użyć [Dockera](https://www.docker.com/) 
### Jeżeli nie masz go zainstalowanego to będziesz musiał go pobrać i zainstalować(logiczne).
Zacznijmy od całkowitego minimum żeby brać udział w części challangy potrzebujesz linuxa(vm, wsl lub natywnego) mac os również zadziała, windows nie.

Jeżeli używasz windowsa wsl(wirtualną maszynę z linuxem) możesz zainstalować uruchamiająć to polecenie w **powershelu(nie cmd) na uprawnieniach administratora**

```powershell
wsl --install
```
Nasępnie wystarczy zrestartować komputer i już jesteś w pełni gotowy do instalacji dockera.

*Ps. aby wywołać shell linuxa wystarczy że w powershellu wpiszesz ```wsl```*

Aby zainstalować dockera(na dowolnym systemie) [użyj tego linku](https://docs.docker.com/engine/install/)

Przeprowadzi cie on przez cały process instalacji oraz pomoże w poprawnej konfiguracji programu
# Uruchamianie obrazów
po zainstalowaniu dockera możesz sprawdzić czy działa przy pomocy specjalnie przygotowanego przez nas w tym celu obrazu [pobierz go tutaj](https://github.com/gpctf/test-image)

Najpierw zbuduj go używająć
```bash
sudo docker build -t ctftestimage ./
```
a następnie uruchom obraz przy pomocy polecenia
```bash
sudo docker run -p 8888:80 ctftestimage
```
wtedy po przejściu na strone [http://localhost:8888](http://localhost:8888) będziesz mógł zobaczyć naszą wspaniałą stronę obrazu testowego

# Uruchamianie maszyny wirtualnej

Do ostatecznego rozwiązania części zadań(bedą one odpowiednio oznaczone) będziesz potrzebował użyć naszej wirtualnej maszyny.
## Uzyskiwanie tokenu do logowania
Zacznijmy od tego iż aby takową uruchomić musisz posiadać token. Uzyskasz go logując sie do discorda(bądż potwierdzając logowanie do aplikacji) [na tej stronie](https://lucky-wall-368009.lm.r.appspot.com/) (jeżeli nam nie wierzysz to sprawdź jest to strona discord.com) następnie zostaniesz przekierowany do nas gdzie dostaniesz swój unikalny token **NIGDY NIKOMU GO NIE PODAWAJ**

Zapisz ten token ponieważ przyda ci sie później

## Uruchamianie maszyny

W celu uruchomienia maszyny będziesz potrzebował narzędzia zwanego netcatem na linuxie możesz je zainstalować uruchamiająć
```bash
sudo apt update && sudo apt install netcat
```

a następnie uruchom polecenie

```bash
nc 34.88.133.94 2137
```
wpisz swój token wybierz maszyne do zadania, potwierdź i postępuj zgodnie z instrukcją wyświetloną ci po pomyślnie zakończonym procesie

Specjalnie w tym celu przygotowaliśmy testowy obraz który możesz uruchomić i przetestować czy wszystko umiesz

**Jeżeli czegokolwiek nie rozumiesz już masz z czymś problem pamiętaj że organizatorzy konkursu zawsze bedą chętni do pomocy**


