---
description: Установщик задает для свойства ProgramFiles64Folder полный путь к предопределенной папке 64-разрядных файлов программы. Для существующего свойства ProgramFilesFolder задается соответствующая 32-разрядная папка.
ms.assetid: 9301628a-3d56-4d0a-aab5-88663742daa1
title: ProgramFiles64Folder, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdb8b85e0a433a3a4b51cfe23ef2de1f75dba09c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675925"
---
# <a name="programfiles64folder-property"></a>ProgramFiles64Folder, свойство

Установщик задает для свойства **ProgramFiles64Folder** полный путь к предопределенной папке 64-разрядных файлов программы. Для существующего свойства [**ProgramFilesFolder**](programfilesfolder.md) задается соответствующая 32-разрядная папка.

## <a name="remarks"></a>Комментарии

Установщик задает это свойство. Например, в 64-разрядной системе Windows значением может быть «C: \\ Program Files». Это свойство не используется в 32-разрядной версии Windows.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Установщик Windows в Windows Server 2003 или Windows XP. Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Свойства](properties.md)
</dt> </dl>

 

 




