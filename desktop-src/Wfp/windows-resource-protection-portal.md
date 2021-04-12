---
description: Защита ресурсов предотвращает замену системных файлов и папок и разделов реестра, необходимых операционной системе. Изменение защищенных ресурсов может привести к сбою приложения или системы.
ms.assetid: 27df9300-8bea-4748-9acd-2c1625093ece
title: защита ресурсов Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff6c89e99b885256c7dd054a12c6a69795d794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347215"
---
# <a name="windows-resource-protection"></a>защита ресурсов Windows

## <a name="purpose"></a>Назначение

Защита ресурсов Windows (WRP) предотвращает замену необходимых системных файлов, папок и разделов реестра, которые устанавливаются в составе операционной системы. Она стала доступной начиная с Windows Server 2008 и Windows Vista. Приложения не должны перезаписывать эти ресурсы, так как они используются системой и другими приложениями. Защита этих ресурсов предотвращает сбои приложений и операционных систем. WRP — это новое имя для защиты файлов Windows (WFP). WRP защищает разделы и папки реестра, а также ключевые системные файлы.

## <a name="where-applicable"></a>Где применимо

Все приложения на базе Windows и программы установки, работающие под управлением Windows Server 2008 или Windows Vista и более поздних операционных систем, должны учитывать WRP. Все приложения на базе Windows, работающие на Microsoft Windows Server 2003 или Windows XP, и программы установки должны знать о WFP.

## <a name="developer-audience"></a>Аудитория разработчиков

API WRP предназначен для использования программистами C/C++. API WRP имеет две функции: [**сфЦисфилепротектед**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) и [**сфЦискэйпротектед**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected).

## <a name="run-time-requirements"></a>Требования к среде выполнения

Для приложений, использующих только функцию [**сфЦисфилепротектед**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) , требуется windows Server 2008, Windows Vista, windows Server 2003 или Windows XP. Для приложений, использующих функцию [**сфЦискэйпротектед**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) , требуется windows Server 2008 или Windows Vista.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                     | Описание                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------|
| [О защита ресурсов Windows](about-windows-file-protection.md)<br/>         | Общие сведения о WRP.<br/>   |
| [Справочник по защита ресурсов Windows](windows-file-protection-reference.md)<br/> | Справочная документация по WRP.<br/> |



 

 

 




