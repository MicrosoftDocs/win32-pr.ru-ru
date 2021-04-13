---
description: Двоичные файлы Windows Server 2003 с пакетом обновления 1 (SP1) совместимы с Windows Vista и Windows Server 2008. Однако двоичные файлы из более ранних версий Windows должны быть перекомпилированы.
ms.assetid: ef40fdf6-b039-4664-bafb-b88c9286c010
title: Перенос приложений резервного копирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85f052996e2c82b11f545bb604b0ed50a886420
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544970"
---
# <a name="porting-backup-applications"></a>Перенос приложений резервного копирования

Двоичные файлы Windows Server 2003 с пакетом обновления 1 (SP1) совместимы с Windows Vista и Windows Server 2008. Однако двоичные файлы из более ранних версий Windows должны быть перекомпилированы.

## <a name="porting-windows-xp-backup-applications-to-windows-vista"></a>Перенос приложений Windows XP Backup на Windows Vista

С момента выпуска Windows XP изменилось несколько интерфейсов VSS. Как минимум, приложения Windows XP должны быть перекомпилированы с помощью файлов заголовков и библиотек из пакета SDK для VSS 7,2 или пакета SDK для Windows Vista или Windows Server 2008.

## <a name="porting-windows-server-2003-sp1-backup-applications-to-windows-vista"></a>Перенос приложений резервного копирования Windows Server 2003 с пакетом обновления 1 (SP1) на Windows Vista

Двоичные файлы Windows Server 2003 с пакетом обновления 1 (SP1) совместимы с Windows Vista и Windows Server 2008. Однако большинство приложений резервного копирования Windows Server 2003 с пакетом обновления 1 (SP1) необходимо обновить для учета новых функций, которые описаны в следующих разделах.

## <a name="compiling-backup-applications-for-windows-vista"></a>Компиляция приложений резервного копирования для Windows Vista

Приложения, использующие интерфейсы, доступные в Windows Server 2003, могут быть скомпилированы с помощью файлов заголовков и библиотек, предоставленных в пакете SDK для VSS 7,2. Для использования новых интерфейсов приложения должны быть перекомпилированы с помощью файлов заголовков и библиотек, входящих в пакет SDK для Windows Vista.

> [!Note]  
> Двоичные файлы, скомпилированные с помощью Windows Vista или Windows Server 2008, несовместимы с Windows Server 2003 с пакетом обновления 1 (SP1) или более ранними версиями Windows.

 

 

 



