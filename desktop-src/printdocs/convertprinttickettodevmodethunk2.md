---
description: Преобразует билет печати в структуру DEVMODE.
ms.assetid: 3b0a6afd-fa9d-434e-a95f-b051296d4567
title: Функция ConvertPrintTicketToDevModeThunk2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertPrintTicketToDevModeThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: e6325ca61d18d571a3a3b346b18f6191b53e43d2ce96799c34a643477123f20c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112684"
---
# <a name="convertprinttickettodevmodethunk2-function"></a>Функция ConvertPrintTicketToDevModeThunk2

\[Эта функция не поддерживается и может быть отключена или удалена в будущих версиях Windows. [**Птконвертпринттиккеттодевмоде**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) предоставляет эквивалентную функциональность, и вместо нее следует использовать.\]

Преобразует билет печати в структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ConvertPrintTicketToDevModeThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      ULONG       cbSize,
  _In_      INT         baseType,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppDevmode,
  _Out_     ULONG       *pcbDevModeLength,
  _Out_opt_ BSTR        *errMsg
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпровидер* \[ окне\]
</dt> <dd>

Маркер открытого поставщика билетов на печать. Этот маркер возвращается функцией [**биндптпровидерсунк**](bindptproviderthunk.md) .

</dd> <dt>

*ппринттиккет* \[ окне\]
</dt> <dd>

Буфер, содержащий билет на печать для преобразования.

</dd> <dt>

*кбсизе* \[ окне\]
</dt> <dd>

Размер буфера (в байтах), переданного в *ппринттиккет*.

</dd> <dt>

*тип BaseType* \[ окне\]
</dt> <dd>

Значение, указывающее, используется ли по умолчанию [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) пользователя или очередь печати по **умолчанию** для предоставления значений для выходного **DEVMODE** , когда *Ппринттиккет* не указывает все возможные параметры для **DEVMODE**. Значение этого параметра должно быть членом перечисления [**едефаултдевмодетипе**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) , приведенным как **int**.

</dd> <dt>

*область действия* \[ окне\]
</dt> <dd>

Значение типа, указывающее область действия *ппринттиккет*. Это значение может указывать одну страницу, весь документ или все документы в задании печати. Значение этого параметра должно быть членом перечисления [**епринттиккетскопе**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , приведенным как **DWORD**.

</dd> <dt>

*ппдевмоде* \[ заполняет\]
</dt> <dd>

Адрес созданного [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea). Эта функция вызывает функцию [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) для выделения буфера. Если буфер больше не нужен, вызывающий объект должен освободить его, вызвав [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*пкбдевмоделенгс* \[ заполняет\]
</dt> <dd>

Размер [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) в байтах, возвращенный в *ппдевмоде*.

</dd> <dt>

*еррмсг* \[ out, необязательно\]
</dt> <dd>

Указатель на строку, указывающую, что, если что-либо, является недопустимым для билета печати в *ппринттиккет*. Если он является допустимым, это **значение равно NULL**. Если *еррмсг* не **равно NULL** , то при возврате функции вызывающий объект должен освободить строку с помощью [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).

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

[**птконвертпринттиккеттодевмоде**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)
</dt> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Функции API очереди печати принтера](printing-and-print-spooler-functions.md)
</dt> </dl>

 

