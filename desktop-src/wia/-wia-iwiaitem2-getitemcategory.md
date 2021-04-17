---
description: Возвращает сведения о категории элемента.
ms.assetid: 4d6f7a6a-280d-4b36-8e1d-8d9fcaa8a1de
title: 'Метод IWiaItem2:: Жетитемкатегори (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemCategory
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: fdf650e8b540fcb9dc58f93f34771462fbc0a5c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711097"
---
# <a name="iwiaitem2getitemcategory-method"></a>Метод IWiaItem2:: Жетитемкатегори

Возвращает сведения о категории элемента.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetItemCategory(
  [out] GUID *pItemCategoryGUID
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*питемкатегоригуид* \[ заполняет\]
</dt> <dd>

Тип: **GUID \** _

Получает указатель на идентификатор GUID, определяющий категорию элемента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Каждый объект [**IWiaItem2**](-wia-iwiaitem2.md) в иерархическом дереве объектов, связанных с аппаратным устройством получения образа Windows (WIA) 2,0, имеет определенную категорию. Этот метод позволяет приложениям указывать категорию любого элемента в иерархическом дереве объектов элементов на устройстве.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




