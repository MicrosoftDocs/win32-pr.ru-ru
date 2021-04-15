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
ms.openlocfilehash: 31d7bceac706715099778cf84af2c3b2ec323880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652033"
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

*Тип* 
</dt> <dd>

Тип источника, например "сеть", "URL-адрес" или "носитель".

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

[**мсисаурцелистклеараллекс**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)
</dt> <dt>

[Не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




