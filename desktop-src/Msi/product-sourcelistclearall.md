---
description: Метод Саурцелистклеаралл, который объект Product удаляет все источники для продукта. Можно указать тип удаляемого источника.
ms.assetid: c8a63b54-7be6-424a-8653-0182b561faab
title: Метод Product. Саурцелистклеаралл
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8718522de7395a4fc6811e210fac0ee7b9f7758f6ea4b632f9fec122ffd5be3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925882"
---
# <a name="productsourcelistclearall-method"></a>Метод Product. Саурцелистклеаралл

Метод **саурцелистклеаралл** , который объект [**Product**](product-object.md) удаляет все источники для продукта. Можно указать тип удаляемого источника.

## <a name="syntax"></a>Синтаксис


```JScript
Product.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Тип* 
</dt> <dd>

Тип удаляемого источника: МСИСАУРЦЕТИПЕ \_ Media, мсисаурцетипе \_ Network или мсисаурцетипе \_ URL.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик 3,0 или более поздней версии на Windows Server 2003, Windows XP и Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ ипродукт определен как 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Продукта**](product-object.md)
</dt> <dt>

[**мсисаурцелистклеарсаурце**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




