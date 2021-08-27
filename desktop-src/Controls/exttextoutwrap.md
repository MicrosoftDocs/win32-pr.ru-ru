---
title: Функция Ексттекстаутврап
description: Рисует текст с использованием текущего выбранного шрифта, цвета фона и цвета текста. При необходимости можно указать измерения, которые будут использоваться для обрезки, непрозрачности или и того, и другого. Эта функция заключает в оболочку вызов ExtTextOut.
ms.assetid: 0804c231-53f9-4de6-b703-0077cdcebcb5
keywords:
- элементы управления Windows функции ексттекстаутврап
topic_type:
- apiref
api_name:
- ExtTextOutWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 934a8d203cf232a339db46e97783e87c075e5bb949ec5d23e20a7b1874ea6ef2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047274"
---
# <a name="exttextoutwrap-function"></a>Функция Ексттекстаутврап

\[**ексттекстаутврап** доступен в Windows XP с пакетом обновления 2 (SP2). Он может быть изменен или недоступен в последующих версиях. Вместо этого рекомендуется использовать [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) напрямую.\]

Рисует текст с использованием текущего выбранного шрифта, цвета фона и цвета текста. При необходимости можно указать измерения, которые будут использоваться для обрезки, непрозрачности или и того, и другого. Эта функция заключает в оболочку вызов [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).

## <a name="syntax"></a>Синтаксис


```C++
BOOL ExtTextOutWrap(
  _In_       HDC     hdc,
  _In_       int     X,
  _In_       int     Y,
  _In_       UINT    uOptions,
  _In_ const RECT    *lprc,
  _In_       LPCTSTR lpString,
  _In_       UINT    cbCount,
  _In_ const INT     *lpDx
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HDC* \[ окне\]
</dt> <dd>

Тип: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Маркер контекста устройства.

</dd> <dt>

*X* \[ в\]
</dt> <dd>

Тип: **int**

Координата x (в логических координатах) точки ссылки, используемой для размещения строки.

</dd> <dt>

*Y* \[ в\]
</dt> <dd>

Тип: **int**

Координата по оси y (в логических координатах) точки ссылки, используемой для размещения строки.

</dd> <dt>

*уоптионс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Значения, указывающие, как использовать определяемый приложением прямоугольник. Полный список параметров см. в разделе [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) .

</dd> <dt>

*ЛПРК* \[ окне\]
</dt> <dd>

Тип: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***

Указатель на необязательную структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , указывающую размеры (в логических координатах) прямоугольника, используемого для обрезки, непрозрачности или и того и другого.

</dd> <dt>

*лпстринг* \[ окне\]
</dt> <dd>

Тип: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Указатель на буфер, содержащий текст для рисования. Строка не должна завершаться нулем, так как *кбкаунт* указывает длину строки.

</dd> <dt>

*кбкаунт* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Длина строки в байтах, на которую указывает *лпстринг*.

</dd> <dt>

*лпдкс* \[ окне\]
</dt> <dd>

Тип: **const [**int**](/windows/desktop/WinProg/windows-data-types) \***

Указатель на необязательный массив значений, указывающий расстояние между источниками смежных ячеек символов. Например,  \[ логические устройства лпдкс x \] разделяют источники ячейки символа x и ячейки символов (x + 1).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **bool** .](/windows/desktop/WinProg/windows-data-types)**

Возвращает ненулевое значение, если строка успешно рисуется. Однако если версия [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) с кодировкой ANSI вызывается с \_ индексом глифа ето \_ , функция возвращает **значение true** , даже если функция ничего не делает.

Если функция выполняется неудачно, возвращается нулевое значение.

Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Комментарии

**Ексттекстаутврап** не экспортируется по имени или объявлено в общедоступном файле заголовка. Чтобы использовать его, необходимо использовать [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) и запросить порядковый номер 417 из ComCtl32.dll для получения указателя на функцию.

Дополнительные замечания см. в разделе [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (версия 6,0 или более поздняя)</dt> </dl> |



 

