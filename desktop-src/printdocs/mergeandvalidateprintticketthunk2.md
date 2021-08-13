---
description: Выполняет слияние двух билетов на печать и возвращает допустимый, действующий билет печати.
ms.assetid: 4aa7b9de-abf2-4781-942e-0b992a6bffed
title: Функция MergeAndValidatePrintTicketThunk2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeAndValidatePrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: 156a242d9aa017cc67106a39db6d86809e0ac6f464566205ead09f69fe1b3b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471677"
---
# <a name="mergeandvalidateprintticketthunk2-function"></a>Функция MergeAndValidatePrintTicketThunk2

\[Эта функция не поддерживается и может быть отключена или удалена в будущих версиях Windows. [**Птмержеандвалидатепринттиккет**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) предоставляет эквивалентную функциональность, и вместо нее следует использовать.\]

Выполняет слияние двух билетов на печать и возвращает допустимый, действующий билет печати.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT MergeAndValidatePrintTicketThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pBasePrintTicket,
  _In_      INT         basePrintTicketLength,
  _In_opt_  BYTE        *pDeltaPrintTicket,
  _In_      INT         deltaPrintTicketLength,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppValidatedPrintTicket,
  _Out_     INT         *pValidatedPrintTicketLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпровидер* \[ окне\]
</dt> <dd>

Маркер открытого поставщика билетов на печать. Этот маркер возвращается функцией [**биндптпровидерсунк**](bindptproviderthunk.md) .

</dd> <dt>

*пбасепринттиккет* \[ окне\]
</dt> <dd>

Буфер, содержащий базовые данные билета на печать, выраженные в формате XML, как описано в [схеме печати](./printschema.md).

</dd> <dt>

*басепринттиккетленгс* \[ окне\]
</dt> <dd>

Размер (в байтах) буфера, на который ссылается *пбасепринттиккет*.

</dd> <dt>

*пделтапринттиккет* \[ в необязательное\]
</dt> <dd>

Буфер, содержащий билет на печать для слияния. Данные билета печати выражаются в формате XML, как описано в [схеме печати](./printschema.md). Значение этого параметра может быть **равно NULL**.

</dd> <dt>

*делтапринттиккетленгс* \[ окне\]
</dt> <dd>

Размер (в байтах) буфера, на который ссылается *пделтапринттиккет*.

</dd> <dt>

*область действия* \[ окне\]
</dt> <dd>

Значение типа, указывающее, является ли область *пделтапринттиккет* и *ппвалидатедпринттиккет* одной страницей, целым документом или всеми документами в задании печати. Значение этого параметра должно быть членом перечисления [**епринттиккетскопе**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , приведенным как **DWORD**.

</dd> <dt>

*ппвалидатедпринттиккет* \[ заполняет\]
</dt> <dd>

Адрес буфера, содержащего Объединенный и проверенный билет печати. Эта функция вызывает функцию [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) для выделения буфера. Если буфер больше не нужен, вызывающий объект должен освободить его, вызвав [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*пвалидатедпринттиккетленгс* \[ заполняет\]
</dt> <dd>

Размер (в байтах) буфера, на который ссылается *ппвалидатедпринттиккет*.

</dd> <dt>

*пбстреррормессаже* \[ out, необязательно\]
</dt> <dd>

Указатель на строку, указывающую, что, если что-либо, является недопустимым для билета печати в *пбасепринттиккет* или *пделтапринттиккет*. Если они оба допустимы, это значение равно **null**. Если *пбстреррормессаже* не **равно NULL** , то при возврате функции вызывающий объект должен освободить строку с помощью [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается значение **\_ ОК**. в противном случае возвращается код ошибки **HRESULT** . Дополнительные сведения о кодах ошибок COM см. в разделе [Обработка ошибок](../com/error-handling-in-com.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Схема печати](./printschema.md)
</dt> <dt>

[**птмержеандвалидатепринттиккет**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)
</dt> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Функции API очереди печати принтера](printing-and-print-spooler-functions.md)
</dt> </dl>

 

