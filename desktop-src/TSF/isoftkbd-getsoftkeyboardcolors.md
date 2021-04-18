---
title: Метод Исофткбд Жетсофткэйбоардколорс (Софткбдк. h)
description: Метод Исофткбд Жетсофткэйбоардколорс извлекает цвет экранной клавиатуры, соответствующий заданному типу цвета.
ms.assetid: d59d249c-a1c4-4d6a-add6-632be55a7549
keywords:
- Платформа служб текстового ввода метода Жетсофткэйбоардколорс
- Платформа текстовых служб метода Жетсофткэйбоардколорс, интерфейс Исофткбд
- Платформа текстовых служб интерфейса Исофткбд, метод Жетсофткэйбоардколорс
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f8f184dc04ddcbef18a9279000b1a68acd35bd3
ms.sourcegitcommit: d6bf2018c588c9782e1eed21b3cdea3523ec6955
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2021
ms.locfileid: "105684714"
---
# <a name="isoftkbdgetsoftkeyboardcolors-method"></a>Метод Исофткбд:: Жетсофткэйбоардколорс

Метод **исофткбд:: жетсофткэйбоардколорс** получает цвет экранной клавиатуры, соответствующий заданному типу цвета.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetSoftKeyboardColors(
  [in]  COLORTYPE colorType,
  [out] COLORREF  *lpColor
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*колортипе* \[ окне\]
</dt> <dd>

Значение типа, указывающее тип цвета, который требуется получить для экранной клавиатуры. Для перечисления [**колортипе**](/windows/win32/api/icm/ne-icm-colortype) определены возможные значения.

</dd> <dt>

*лпколор* \[ заполняет\]
</dt> <dd>

Указатель на буфер, в котором этот метод получает 32-битное значение [**COLORREF**](/windows/desktop/gdi/colorref) , УКАЗЫВАЮЩЕЕ цвет RGB.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Значение                                                                                        | Описание                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Метод успешно выполнен.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Один из параметров недопустим.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| Распространяемые компоненты<br/>          | TSF 1,0 в Windows 2000 профессиональная<br/>                                        |
| Header<br/>                   | <dl> <dt>Софткбдк. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Софткбд. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**исофткбд**](isoftkbd.md)
</dt> <dt>

[**Исофткбд:: Сетсофткэйбоардколорс**](/windows/desktop/TSF/isoftkbd-setsoftkeyboardcolors)
</dt> <dt>

[**колортипе**](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> </dl>

 

