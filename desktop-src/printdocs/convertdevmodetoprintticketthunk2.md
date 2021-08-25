---
description: Преобразует структуру DEVMODE в билет печати.
ms.assetid: c03371f8-a978-4fb7-82cc-f76a65f3904c
title: Функция ConvertDevModeToPrintTicketThunk2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertDevModeToPrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: d5aea99e54a43eb35f76c719da885f8d7ae0352d47ecff62b7df38de30410025
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950394"
---
# <a name="convertdevmodetoprintticketthunk2-function"></a>Функция ConvertDevModeToPrintTicketThunk2

\[Эта функция не поддерживается и может быть отключена или удалена в будущих версиях Windows. [**Птконвертдевмодетопринттиккет**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) предоставляет эквивалентную функциональность, и вместо нее следует использовать.\]

Преобразует структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) в билет печати.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ConvertDevModeToPrintTicketThunk2(
  _In_  HPTPROVIDER hProvider,
  _In_  BYTE        *pDevmode,
  _In_  ULONG       cbSize,
  _In_  DWORD       scope,
  _Out_ BYTE        **ppPrintTicket,
  _Out_ INT         *pcbPrintTicketLength
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпровидер* \[ окне\]
</dt> <dd>

Маркер открытого поставщика билетов на печать. Этот маркер возвращается функцией [**биндптпровидерсунк**](bindptproviderthunk.md) .

</dd> <dt>

*пдевмоде* \[ окне\]
</dt> <dd>

Указатель на [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) для преобразования.

</dd> <dt>

*кбсизе* \[ окне\]
</dt> <dd>

Размер (в байтах) [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , переданного в *пдевмоде*.

</dd> <dt>

*область действия* \[ окне\]
</dt> <dd>

Значение типа, указывающее область действия *пппринттиккет*. Это значение может указывать одну страницу, весь документ или все документы в задании печати. Значение этого параметра должно быть членом перечисления [**епринттиккетскопе**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , приведенным как **DWORD**.

</dd> <dt>

*пппринттиккет* \[ заполняет\]
</dt> <dd>

Адрес буфера, содержащего билет на печать, представляющий [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , переданный в *пдевмоде*. Эта функция вызывает функцию [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) для выделения буфера. Если буфер больше не нужен, вызывающий объект должен освободить его, вызвав [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*пкбпринттиккетленгс* \[ заполняет\]
</dt> <dd>

Размер билета печати (в байтах), возвращенного в *пппринттиккет*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается значение **\_ ОК**. в противном случае возвращается код ошибки **HRESULT** . Дополнительные сведения о кодах ошибок COM см. в разделе [Обработка ошибок](../com/error-handling-in-com.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Схема печати](./printschema.md)
</dt> <dt>

[**птконвертдевмодетопринттиккет**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)
</dt> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Функции API очереди печати принтера](printing-and-print-spooler-functions.md)
</dt> </dl>

 

