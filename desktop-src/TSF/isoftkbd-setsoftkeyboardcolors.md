---
title: Метод Исофткбд Сетсофткэйбоардколорс (Софткбдк. h)
description: Метод Исофткбд Сетсофткэйбоардколорс задает цвет экранной клавиатуры для указанного типа цвета.
ms.assetid: 1abbff35-a5ef-4119-9367-60b6e0961c59
keywords:
- Платформа служб текстового ввода метода Сетсофткэйбоардколорс
- Платформа текстовых служб метода Сетсофткэйбоардколорс, интерфейс Исофткбд
- Платформа текстовых служб интерфейса Исофткбд, метод Сетсофткэйбоардколорс
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b572d62895a4f5df503df3ed78bfcf931af331ded25596267f0dd5b4286a4c4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877375"
---
# <a name="isoftkbdsetsoftkeyboardcolors-method"></a>Метод Исофткбд:: Сетсофткэйбоардколорс

Метод **исофткбд:: сетсофткэйбоардколорс** задает цвет экранной клавиатуры для указанного типа цвета.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetSoftKeyboardColors(
  [in] COLORTYPE colorType,
  [in] COLORREF  Color
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*колортипе* \[ окне\]
</dt> <dd>

Значение типа, указывающее тип цвета для экранной клавиатуры. Для перечисления [**колортипе**](/windows/win32/api/icm/ne-icm-colortype) определены возможные значения.

</dd> <dt>

*Цветовая палитра* \[ окне\]
</dt> <dd>

32-битное значение [**COLORREF**](/windows/desktop/gdi/colorref) , УКАЗЫВАЮЩЕЕ цвет RGB.

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
| Распространяемые компоненты<br/>          | TSF 1,0 на Windows 2000 Professional<br/>                                        |
| Header<br/>                   | <dl> <dt>Софткбдк. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Софткбд. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**исофткбд**](isoftkbd.md)
</dt> <dt>

[**Исофткбд:: Жетсофткэйбоардколорс**](isoftkbd-getsoftkeyboardcolors.md)
</dt> <dt>

[**колортипе**](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> </dl>

 

