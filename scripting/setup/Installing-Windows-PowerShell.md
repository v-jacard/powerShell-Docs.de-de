---
title: Installieren von Windows PowerShell
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6fbb0409-5a54-48ec-95e6-7f8b7d8c4969
---
# Installieren von Windows PowerShell
Windows® 8 und Windows Server® 2012 enthalten Windows PowerShell 3.0 und alle erforderlichen Komponenten. Das System enthält auch Windows PowerShell 2.0 Engine für die Abwärtskompatibilität mit Hostprogrammen, die Windows PowerShell 3.0 nicht verwenden können.

In diesem Thema wird erläutert, wie Sie Windows PowerShell 3.0 auf älteren Systemen installieren und die erforderlichen Features installieren und aktivieren.

Dieses Thema enthält die folgenden Abschnitte:

-   [Installieren von Windows PowerShell unter Windows 8 und Windows Server 2012](Installing-Windows-PowerShell.md#BKMK_InstallingOnWindows8andWindowsServer2012)

-   [Installieren von Windows PowerShell unter Windows 7 und Windows Server 2008 R2](Installing-Windows-PowerShell.md#BKMK_InstallingOnWindows7andWindowsServer2008R2)

-   [Installieren von Windows PowerShell unter Windows Server 2008](Installing-Windows-PowerShell.md#BKMK_InstallingOnWindowsServer2008LH)

-   [Installieren von Windows PowerShell unter Server Core](Installing-Windows-PowerShell.md#BKMK_InstallingOnServerCore)

-   [Bereitstellen von Windows PowerShell Web Access](https://technet.microsoft.com/en-us/library/639d0eff-98a3-4124-b52c-26921ebd98b0)

-   [Installieren des Windows PowerShell 2.0-Moduls](Installing-the-Windows-PowerShell-2.0-Engine.md)

## <a name="BKMK_InstallingOnWindows8andWindowsServer2012"></a>Installieren von Windows PowerShell unter Windows 8 und Windows Server 2012
Windows PowerShell 3.0 wird installiert, konfiguriert und einsatzbereit geliefert. Windows PowerShell Integrated Scripting Environment (ISE) ist installiert und aktiviert. Weitere Informationen zum Starten von Windows PowerShell finden Sie unter [Starten von Windows PowerShell unter Windows 8](https://technet.microsoft.com/en-us/library/d7be1668-8617-4890-ad90-dd9765fbd2c3) und [Starten von Windows PowerShell unter Windows Server 2012](https://technet.microsoft.com/en-us/library/4fc0110a-cc0c-42a4-bbb5-3cc89a0fc968)..

## <a name="BKMK_InstallingOnWindows7andWindowsServer2008R2"></a>Installieren von Windows PowerShell unter Windows 7 und Windows Server 2008 R2
Diese Anleitung erläutert die Installation von Windows PowerShell 3.0 auf Computern mit Windows 7 mit Service Pack 1 und Windows Server 2008 R2 mit Service Pack 1. Für Computer mit der Installationsoption Server Core von Windows Server 2008 R2 finden Sie nachstehend gesonderte Installationsanweisungen.

#### Vorbereiten der Installation

-   Deinstallieren Sie vor der Installation von Windows Management Framework 3.0 alle früheren Versionen von Windows Management Framework 3.0.

#### So installieren Sie Windows PowerShell 3.0

1.  Installieren Sie die vollständige Installation von Microsoft .NET Framework 4 (dotNetFx40\_Full\_setup.exe), die Sie im Microsoft Download Center unter [http://go.microsoft.com/fwlink/?LinkID=212547](http://go.microsoft.com/fwlink/?LinkID=212547) finden..

    Oder installieren Sie Microsoft .NET Framework 4.5 (dotNetFx45\_Full\_setup.exe), das Sie im Microsoft Download Center unter [http://go.microsoft.com/fwlink/?LinkID=242919](http://go.microsoft.com/fwlink/?LinkID=242919) finden..

2.  Installieren Sie Windows Management Framework 3.0 aus dem Microsoft Download Center unter [http://go.microsoft.com/fwlink/?LinkID=240290](http://go.microsoft.com/fwlink/?LinkID=240290)..

Weitere Informationen zum Starten von Windows PowerShell 3.0 finden Sie unter [Starten von Windows PowerShell unter früheren Versionen von Windows](Starting-Windows-PowerShell-on-Earlier-Versions-of-Windows.md)..

## <a name="BKMK_InstallingOnServerCore"></a>Installieren von Windows PowerShell unter Server Core
Diese Anleitungen erläutern die Installation von Windows PowerShell 3.0 auf Computern mit der Installationsoption Server Core von Windows Server 2008 R2 mit Service Pack 1.

In den ersten Schritten des Verfahrens werden DISM-Befehle (Deployment Image Servicing and Management, Abbildverwaltung für die Bereitstellung) zum Installieren von Microsoft .NET Framework 2.0 für Server Core und Windows PowerShell 2.0 verwendet. Diese Programme sind Voraussetzungen für Windows Management Framework 3.0, das in einem späteren Schritt installiert wird.

#### Vorbereiten der Installation

-   Deinstallieren Sie vor der Installation von Windows Management Framework 3.0 alle früheren Versionen von Windows Management Framework 3.0.

#### So installieren Sie Windows PowerShell 3.0

1.  Starten Sie „Cmd.exe“.

2.  Führen Sie die folgenden DISM-Befehle aus. Diese Befehle führen zur Installation von .NET Framework 2.0 und Windows PowerShell 2.0.

    ```
    dism /online /enable-feature:NetFx2-ServerCore
    dism /online /enable-feature:MicrosoftWindowsPowerShell
    dism /online /enable-feature:NetFx2-ServerCore-WOW64
    ```

3.  Installieren Sie die vollständige Installation von Microsoft .NET Framework 4.0 für Server Core, die Sie im Microsoft Download Center unter [http://go.microsoft.com/fwlink/?LinkID=248450](http://go.microsoft.com/fwlink/?LinkID=248450) finden..

4.  Installieren Sie Windows Management Framework 3.0 aus dem Microsoft Download Center unter [http://go.microsoft.com/fwlink/?LinkID=240290](http://go.microsoft.com/fwlink/?LinkID=240290)..

## <a name="BKMK_InstallingOnWindowsServer2008LH"></a>Installieren von Windows PowerShell unter Windows Server 2008
Diese Anleitung erläutert die Installation von Windows PowerShell 3.0 auf Computern mit Windows Server 2008 mit Service Pack 2.

Auf Windows Server 2008-Systemen ist Windows Management Framework (Windows PowerShell 2.0, KB 968930) eine Voraussetzung für Windows Management Framework 3.0. Das Feature „Erweiterter Schutz für Authentifizierung“ schützt den Computer vor Angriffen mittels Weiterleitung der Authentifizierung und ermöglicht beim Starten von Remotesitzungen die Verwendung des **UseSSL**-Parameters. Verwenden Sie das folgende Verfahren, um Windows PowerShell 3.0 und Windows PowerShell 2.0 Engine zu installieren.

#### Vorbereiten der Installation

-   Deinstallieren Sie vor der Installation von Windows Management Framework 3.0 alle früheren Versionen von Windows Management Framework 3.0.

#### So installieren Sie Windows PowerShell 3.0

1.  Installieren Sie Microsoft .NET Framework 3.5 mit Service Pack 1, das Sie im Microsoft Download Center unter [http://go.microsoft.com/fwlink/?LinkID=242910](http://go.microsoft.com/fwlink/?LinkID=242910) finden..

2.  Installieren Sie Windows Management Framework (Windows PowerShell 2.0, KB 968930), das Sie im Microsoft Center unter [http://go.microsoft.com/fwlink/?LinkId=243035](http://go.microsoft.com/fwlink/?LinkId=243035) finden..

3.  Installieren Sie die vollständige Installation von Microsoft .NET Framework 4 (dotNetFx40\_Full\_setup.exe), die Sie im Microsoft Download Center unter [http://go.microsoft.com/fwlink/?LinkID=212547](http://go.microsoft.com/fwlink/?LinkID=212547) finden..

    Oder installieren Sie Microsoft .NET Framework 4.5 (dotNetFx45\_Full\_setup.exe), das Sie im Microsoft Download Center unter [http://go.microsoft.com/fwlink/?LinkID=242919](http://go.microsoft.com/fwlink/?LinkID=242919) finden..

4.  Installieren Sie „Erweiterter Schutz für Authentifizierung“ (KB 968389), das Sie unter [http://go.microsoft.com/fwlink/?LinkID=186398](http://go.microsoft.com/fwlink/?LinkID=186398) finden..

5.  Installieren Sie Windows Management Framework 3.0 aus dem Microsoft Download Center unter [http://go.microsoft.com/fwlink/?LinkID=240290](http://go.microsoft.com/fwlink/?LinkID=240290)..

## Weitere Informationen
[Windows PowerShell-Systemanforderungen](Windows-PowerShell-System-Requirements.md)
[Starten von Windows PowerShell [ps]](https://technet.microsoft.com/en-us/library/8ec8c2d7-8e7c-4722-a3d2-498fe5739a8e)



<!--HONumber=May16_HO2-->


