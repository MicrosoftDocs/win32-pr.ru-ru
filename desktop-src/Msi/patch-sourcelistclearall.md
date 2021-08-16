---
description: Метод Саурцелистклеаралл объекта Patch очищает полный исходный список всех источников указанного типа для исправления. Принимает тип в качестве параметра. Этот метод вызывает Мсисаурцелистклеараллекс.
ms.assetid: 9458a3db-8eaa-4067-875f-8fac68bdf1f8
title: Метод PATCH. Саурцелистклеаралл
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ae7de8c0a830000b3100e84cacbf088fefb592ddaa912a7737a35ea009a3cfe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942304"
---
# <a name="patchsourcelistclearall-method"></a>Метод PATCH. Саурцелистклеаралл

Метод **саурцелистклеаралл** объекта [**Patch**](patch-object.md) очищает полный исходный список всех источников указанного типа для исправления. Принимает *тип* в качестве параметра. Этот метод вызывает [**мсисаурцелистклеараллекс**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa).

## <a name="syntax"></a>Синтаксис


```JScript
Patch.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Type* 
</dt> <dd>

Тип источника, например "сеть", "URL-адрес" или "носитель".

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик 3,0 или более поздней версии на Windows Server 2003, Windows XP и Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ ипатч определен как 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Обновление**](patch-object.md)
</dt> <dt>

[**мсисаурцелистклеараллекс**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)
</dt> <dt>

[не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




