---
description: создает объект перечислителя и передает обратно указатель на его интерфейс IEnumWiaItem2 для папок с элементами в дереве IWiaItem2 устройства Windowsного получения изображений (WIA) 2,0.
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
ms.openlocfilehash: 921a6b6e85f906ef62683038b2bb28dd484d58fd20600b2ff85ae594fafb3cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440422"
---
# <a name="iwiaitem2enumchilditems-method"></a>Метод IWiaItem2:: Енумчилдитемс

создает объект перечислителя и передает обратно указатель на его интерфейс [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) для папок с элементами в дереве [**IWiaItem2**](-wia-iwiaitem2.md) устройства Windowsного получения изображений (WIA) 2,0.

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

Тип: **константа \* GUID**

Указывает указатель на категорию, для которой перечисляются дочерние узлы. Если **значение равно NULL**, то перечисляются все дочерние узлы.

</dd> <dt>

*ppIEnumWiaItem2* \[ заполняет\]
</dt> <dd>

Тип: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***

Получает адрес указателя на интерфейс [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) , создаваемый этим методом.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Система времени выполнения WIA 2,0 представляет каждое аппаратное устройство WIA 2,0 как иерархическое дерево объектов [**IWiaItem2**](-wia-iwiaitem2.md) . Метод **IWiaItem2:: енумчилдитемс** позволяет приложениям перечислять дочерние элементы в текущем элементе. Однако его можно применить только к элементам, которые являются папками.

Если папка не пуста, она содержит поддерево объектов [**IWiaItem2**](-wia-iwiaitem2.md) . Метод **IWiaItem2:: енумчилдитемс** перечисляет все элементы, содержащиеся в папке. Он сохраняет указатель на перечислитель в параметре *ppIEnumWiaItem2* . Приложения используют указатель перечислителя для выполнения перечисления дочерних элементов объекта.

Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают с помощью параметра *ppIEnumWiaItem2* .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
