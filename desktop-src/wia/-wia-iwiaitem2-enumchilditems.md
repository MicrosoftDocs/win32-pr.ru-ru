---
description: Создает объект перечислителя и передает обратно указатель на его интерфейс IEnumWiaItem2 для папок с элементами в дереве IWiaItem2 устройства Windows Image (WIA) 2,0.
ms.assetid: 0862bb6f-0464-491a-8cad-60b92d9609f1
title: 'Метод IWiaItem2:: Енумчилдитемс (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumChildItems
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2de76d9bf43d10e08e5a85cd2a32d6b377680d18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497553"
---
# <a name="iwiaitem2enumchilditems-method"></a>Метод IWiaItem2:: Енумчилдитемс

Создает объект перечислителя и передает обратно указатель на его интерфейс [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) для папок с элементами в дереве [**IWiaItem2**](-wia-iwiaitem2.md) устройства Windows Image (WIA) 2,0.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EnumChildItems(
  [in]  const GUID          *pCategoryGUID,
  [out]       IEnumWiaItem2 **ppIEnumWiaItem2
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкатегоригуид* \[ окне\]
</dt> <dd>

Тип: **константа \* GUID* _

Указывает указатель на категорию, для которой перечисляются дочерние узлы. Если значение _ * NULL * *, то перечисляются все дочерние узлы.

</dd> <dt>

*ppIEnumWiaItem2* \[ заполняет\]
</dt> <dd>

Тип: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***

Получает адрес указателя на интерфейс [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) , создаваемый этим методом.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Система времени выполнения WIA 2,0 представляет каждое аппаратное устройство WIA 2,0 как иерархическое дерево объектов [**IWiaItem2**](-wia-iwiaitem2.md) . Метод **IWiaItem2:: енумчилдитемс** позволяет приложениям перечислять дочерние элементы в текущем элементе. Однако его можно применить только к элементам, которые являются папками.

Если папка не пуста, она содержит поддерево объектов [**IWiaItem2**](-wia-iwiaitem2.md) . Метод **IWiaItem2:: енумчилдитемс** перечисляет все элементы, содержащиеся в папке. Он сохраняет указатель на перечислитель в параметре *ppIEnumWiaItem2* . Приложения используют указатель перечислителя для выполнения перечисления дочерних элементов объекта.

Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают с помощью параметра *ppIEnumWiaItem2* .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
