---
description: Извлекает возможности принтеров, отформатированные в соответствии с XML-схемой печати.
ms.assetid: 15219c19-b64c-4c51-9357-15a797557693
title: Функция GetPrintCapabilitiesThunk2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintCapabilitiesThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: eb60f1cdabad6287e236fc099fc304e9e7de83ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702333"
---
# <a name="getprintcapabilitiesthunk2-function"></a>Функция GetPrintCapabilitiesThunk2

\[Эта функция не поддерживается и может быть отключена или удалена в будущих версиях Windows. [**Птжетпринткапабилитиес**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities) предоставляет эквивалентную функциональность, и вместо нее следует использовать.\]

Получает возможности принтера, отформатированные в соответствии с XML- [схемой печати](./printschema.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetPrintCapabilitiesThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      INT         cbPrintTicket,
  _Out_     BYTE        **ppbPrintCapabilities,
  _Out_     INT         *pcbPrintCapabilitiesLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
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

Буфер, содержащий данные билета на печать, выраженные в формате XML, как описано в [схеме печати](./printschema.md).

</dd> <dt>

*кбпринттиккет* \[ окне\]
</dt> <dd>

Размер (в байтах) буфера, на который ссылается *ппринттиккет*.

</dd> <dt>

*ппбпринткапабилитиес* \[ заполняет\]
</dt> <dd>

Адрес буфера, выделенный этой функцией и содержащий допустимые сведения о возможностях печати, закодированные как XML. Эта функция вызывает функцию [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) для выделения буфера. Если буфер больше не нужен, вызывающий объект должен освободить его, вызвав [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*пкбпринткапабилитиесленгс* \[ заполняет\]
</dt> <dd>

Размер (в байтах) буфера, на который ссылается *ппбпринткапабилитиес*.

</dd> <dt>

*пбстреррормессаже* \[ out, необязательно\]
</dt> <dd>

Указатель на строку, указывающую, что, если что-либо является недопустимым для *ппринттиккет*. Если он является допустимым, это значение равно **null**. Если *пбстреррормессаже* не **равно NULL** , то при возврате функции вызывающий объект должен освободить строку с помощью [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается значение **\_ ОК**. в противном случае возвращается код ошибки **HRESULT** . Дополнительные сведения о кодах ошибок COM см. в разделе [Обработка ошибок](../com/error-handling-in-com.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**птжетпринткапабилитиес**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)
</dt> <dt>

[Схема печати](./printschema.md)
</dt> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Функции API очереди печати принтера](printing-and-print-spooler-functions.md)
</dt> </dl>

 

