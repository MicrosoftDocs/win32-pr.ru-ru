---
description: Метод Саурцелистклеармедиадиск объекта Product удаляет указанный диск из набора зарегистрированных дисков для продукта. Принимает DiskID в качестве параметра. Этот метод вызывает Мсисаурцелистклеармедиадиск.
ms.assetid: 7eec644e-5127-4c17-a8bd-6b0eb091c8aa
title: Метод Product. Саурцелистклеармедиадиск
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a607591f45208854118b0f97849cd7072e484bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651692"
---
# <a name="productsourcelistclearmediadisk-method"></a>Метод Product. Саурцелистклеармедиадиск

Метод **саурцелистклеармедиадиск** объекта [**Product**](product-object.md) удаляет указанный диск из набора зарегистрированных дисков для продукта. Принимает *DiskID* в качестве параметра. Этот метод вызывает [**мсисаурцелистклеармедиадиск**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska).

## <a name="syntax"></a>Синтаксис


```JScript
Product.SourceListClearMediaDisk(
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
| IID<br/>     | IID \_ ипродукт определен как 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Продукта**](product-object.md)
</dt> <dt>

[**мсисаурцелистклеармедиадиск**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)
</dt> <dt>

[Не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




