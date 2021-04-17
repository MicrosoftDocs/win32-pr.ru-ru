---
description: Метод Екстрактпатчксмлдата объекта Installer извлекает сведения из исправления в виде XML-строки. Эти сведения можно использовать для определения того, применяется ли исправление к целевой системе. Этот метод вызывает Мсиекстрактпатчксмлдата.
ms.assetid: 85940940-2002-4cb1-8e29-ba2374bf3796
title: Метод Installer. Екстрактпатчксмлдата
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ExtractPatchXMLData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 69c17236c0a4cd96820e0366df51b28cf47ecfb0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651624"
---
# <a name="installerextractpatchxmldata-method"></a>Метод Installer. Екстрактпатчксмлдата

Метод **екстрактпатчксмлдата** объекта [**Installer**](installer-object.md) извлекает сведения из исправления в виде XML-строки. Эти сведения можно использовать для определения того, применяется ли исправление к целевой системе. Этот метод вызывает [**мсиекстрактпатчксмлдата**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).

## <a name="syntax"></a>Синтаксис


```JScript
Installer.ExtractPatchXMLData(
  PatchPath
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*патчпас* 
</dt> <dd>

Полный путь к исправлению, из которого извлекаются сведения о применимости.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Установщик Windows 3,0 или более поздней версии в Windows Server 2003 или Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мсиекстрактпатчксмлдата**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> <dt>

[Не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




