---
description: Метод Саурцелистклеарсаурце удаляет сеть или источник URL-адреса. Принимает тип, исходный путь и источник, в качестве параметров для удаления. Этот метод вызывает Мсисаурцелистклеарсаурце.
ms.assetid: a55676d4-795d-4ffe-8621-ef47c16a936c
title: Метод Product. Саурцелистклеарсаурце
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9adeb342aa47162905814979eb29853edd1c5bc660e3771f3beabb8a485c6060
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376697"
---
# <a name="productsourcelistclearsource-method"></a>Метод Product. Саурцелистклеарсаурце

Метод **саурцелистклеарсаурце** удаляет сеть или источник URL-адреса. Принимает *тип* *, исходный путь и источник*, в качестве параметров для удаления. Этот метод вызывает [**мсисаурцелистклеарсаурце**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).

## <a name="syntax"></a>Синтаксис


```JScript
Product.SourceListClearSource(
  Type,
  SourcePath
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Type* 
</dt> <dd>

Тип удаляемого источника: МСИСАУРЦЕТИПЕ \_ Network или мсисаурцетипе \_ URL.

</dd> <dt>

*SourcePath* 
</dt> <dd>

Путь к удаляемому источнику.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик 3,0 или более поздней версии на Windows Server 2003, Windows XP и Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ ипродукт определен как 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Продукта**](product-object.md)
</dt> <dt>

[**мсисаурцелистклеарсаурце**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




