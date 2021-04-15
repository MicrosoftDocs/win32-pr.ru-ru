---
description: Метод Саурцелистклеармедиадиск объекта Patch удаляет указанный диск из набора зарегистрированных дисков для исправления. Принимает DiskID в качестве параметра. Этот метод вызывает Мсисаурцелистклеармедиадиск.
ms.assetid: fc52ecb9-2c79-497b-b551-0d3c4f584e86
title: Метод PATCH. Саурцелистклеармедиадиск
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 722b4573d89214312e77e4fde78e1905aefa885f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651709"
---
# <a name="patchsourcelistclearmediadisk-method"></a>Метод PATCH. Саурцелистклеармедиадиск

Метод **саурцелистклеармедиадиск** объекта [**Patch**](patch-object.md) удаляет указанный диск из набора зарегистрированных дисков для исправления. Принимает *DiskID* в качестве параметра. Этот метод вызывает [**мсисаурцелистклеармедиадиск**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska).

## <a name="syntax"></a>Синтаксис


```JScript
Patch.SourceListClearMediaDisk(
  Diskid
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*DiskID* 
</dt> <dd>

Этот параметр задает идентификатор удаляемого диска.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ ипатч определен как 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Защиты**](patch-object.md)
</dt> <dt>

[**мсисаурцелистклеармедиадиск**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)
</dt> <dt>

[Не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




