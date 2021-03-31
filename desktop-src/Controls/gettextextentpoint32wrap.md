---
title: Функция GetTextExtentPoint32Wrap
description: Вычисление ширины и высоты указанной строки текста. Эта функция заключает в оболочку вызов Жеттекстекстентпоинт.
ms.assetid: 156f9344-6071-451c-94c7-63f369a5573a
keywords:
- Элементы управления Windows для функций GetTextExtentPoint32Wrap
topic_type:
- apiref
api_name:
- GetTextExtentPoint32Wrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6a0db92ad019950cf8be0a72260da75acc06779
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801234"
---
# <a name="gettextextentpoint32wrap-function"></a>Функция GetTextExtentPoint32Wrap

\[**GetTextExtentPoint32Wrap** доступен в Windows XP с пакетом обновления 2 (SP2). Он может быть изменен или недоступен в последующих версиях. Вместо этого рекомендуется использовать [**жеттекстекстентпоинт**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa) напрямую.\]

Вычисление ширины и высоты указанной строки текста. Эта функция заключает в оболочку вызов [**жеттекстекстентпоинт**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).

## <a name="syntax"></a>Синтаксис


```C++
BOOL GetTextExtentPoint32Wrap(
  _In_  HDC     hdc,
  _In_  LPCTSTR lpString,
  _In_  UINT    cbCount,
  _Out_ LPSIZE  lpSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HDC* \[ окне\]
</dt> <dd>

Тип: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Маркер контекста устройства.

</dd> <dt>

*лпстринг* \[ окне\]
</dt> <dd>

Тип: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Указатель на буфер, содержащий текст для рисования. Строка не должна завершаться нулем, так как *кбкаунт* указывает длину строки.

</dd> <dt>

*кбкаунт* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Длина строки в байтах, на которую указывает параметр *лпстринг*.

</dd> <dt>

*лпсизе* \[ заполняет\]
</dt> <dd>

Тип: **лпсизе**

При возврате из этого метода содержит указатель на структуру [**размера**](/previous-versions//dd145106(v=vs.85)) , содержащую измерения строки в логических единицах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **bool** .](/windows/desktop/WinProg/windows-data-types)**

При успешном выполнении возвращает ненулевое значение. в противном случае — значение 0.

Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Комментарии

**GetTextExtentPoint32Wrap** не экспортируется по имени или объявлено в общедоступном файле заголовка. Чтобы использовать его, необходимо использовать [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) и запросить порядковый номер 420 из ComCtl32.dll для получения указателя на функцию.

Дополнительные замечания см. в разделе [**жеттекстекстентпоинт**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                                  |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (версия 5,81 или более поздняя)</dt> </dl> |



 

