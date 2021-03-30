---
description: Заполняет массив указателей на интерфейсы IWiaItem2.
ms.assetid: 35fd5bdf-7e6c-431f-a9c6-62a86ee05f95
title: 'Метод IEnumWiaItem2:: Next (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Next
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2e8800ead0c8f0abaddd0f055f31962d4d55d14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263314"
---
# <a name="ienumwiaitem2next-method"></a>Метод IEnumWiaItem2:: Next

Заполняет массив указателей на интерфейсы [**IWiaItem2**](-wia-iwiaitem2.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Next(
  [in]      ULONG     cElt,
  [out]     IWiaItem2 **ppIWiaItem2,
  [in, out] ULONG     *pcEltFetched
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*cElt* \[ окне\]
</dt> <dd>

Тип: **ulong**

Указывает количество элементов массива в массиве, указанное параметром *ppIWiaItem2* .

</dd> <dt>

*ppIWiaItem2* \[ заполняет\]
</dt> <dd>

Тип: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Получает адрес массива указателей интерфейса [**IWiaItem2**](-wia-iwiaitem2.md) . **IEnumWiaItem2:: Next** заполняет этот массив указателями интерфейса.

</dd> <dt>

*пцелтфетчед* \[ в, out\]
</dt> <dd>

Тип: **ulong \** _

На выходе этот параметр получает число указателей интерфейса, которые фактически хранятся в массиве, указанном параметром _ppIWiaItem2 *. По завершении перечисления этот параметр содержит нуль.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Система времени выполнения Windows Image (WIA) 2,0 представляет устройство WIA 2,0 как иерархическое дерево объектов [**IWiaItem2**](-wia-iwiaitem2.md) . Приложения используют метод **IEnumWiaItem2:: Next** для получения указателя на интерфейс **IWiaItem2** для каждого элемента в текущей папке в дереве объектов **IWiaItem2** аппаратного устройства.

Чтобы получить список указателей, приложение передает массив [**IWiaItem2ных**](-wia-iwiaitem2.md) указателей интерфейса, которые он выделяет. Он также передает количество элементов массива в параметре *cElt*. Метод **IEnumWiaItem2:: Next** заполняет массив указателями на интерфейсы **IWiaItem2** .

До завершения процесса перечисления метод **IEnumWiaItem2:: Next** возвращает значение S \_ . Каждый раз он устанавливает значение, на которое указывает, *пцелтфетчед* число элементов, вставляемых в массив. Когда **IEnumWiaItem2:: Next** завершает процесс перечисления объектов [**IWiaItem2**](-wia-iwiaitem2.md) , он возвращает \_ значение false и задает для расположения памяти, на которое указывает *пцелтфетчед* , значение 0.

Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают с помощью параметра *ppIWiaItem2* .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
