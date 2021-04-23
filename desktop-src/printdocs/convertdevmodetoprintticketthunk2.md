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
ms.openlocfilehash: f13d597a11a4d6cfd1ad6f5d70b3a386560f5106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673631"
---
# <a name="convertdevmodetoprintticketthunk2-function"></a><span data-ttu-id="8f176-103">Функция ConvertDevModeToPrintTicketThunk2</span><span class="sxs-lookup"><span data-stu-id="8f176-103">ConvertDevModeToPrintTicketThunk2 function</span></span>

<span data-ttu-id="8f176-104">\[Эта функция не поддерживается и может быть отключена или удалена в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="8f176-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="8f176-105">[**Птконвертдевмодетопринттиккет**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) предоставляет эквивалентную функциональность, и вместо нее следует использовать.\]</span><span class="sxs-lookup"><span data-stu-id="8f176-105">[**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="8f176-106">Преобразует структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) в билет печати.</span><span class="sxs-lookup"><span data-stu-id="8f176-106">Converts a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure to a print ticket.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f176-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f176-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="8f176-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8f176-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f176-109">*хпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8f176-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f176-110">Маркер открытого поставщика билетов на печать.</span><span class="sxs-lookup"><span data-stu-id="8f176-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="8f176-111">Этот маркер возвращается функцией [**биндптпровидерсунк**](bindptproviderthunk.md) .</span><span class="sxs-lookup"><span data-stu-id="8f176-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="8f176-112">*пдевмоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8f176-112">*pDevmode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f176-113">Указатель на [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) для преобразования.</span><span class="sxs-lookup"><span data-stu-id="8f176-113">A pointer to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) to convert.</span></span>

</dd> <dt>

<span data-ttu-id="8f176-114">*кбсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8f176-114">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f176-115">Размер (в байтах) [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , переданного в *пдевмоде*.</span><span class="sxs-lookup"><span data-stu-id="8f176-115">The size, in bytes, of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passed in *pDevmode*.</span></span>

</dd> <dt>

<span data-ttu-id="8f176-116">*область действия* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8f176-116">*scope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f176-117">Значение типа, указывающее область действия *пппринттиккет*.</span><span class="sxs-lookup"><span data-stu-id="8f176-117">A value that specifies the scope of *ppPrintTicket*.</span></span> <span data-ttu-id="8f176-118">Это значение может указывать одну страницу, весь документ или все документы в задании печати.</span><span class="sxs-lookup"><span data-stu-id="8f176-118">This value can specify a single page, an entire document, or all documents in the print job.</span></span> <span data-ttu-id="8f176-119">Значение этого параметра должно быть членом перечисления [**епринттиккетскопе**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , приведенным как **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="8f176-119">The value of this parameter must be a member of the [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) enumeration, cast as a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="8f176-120">*пппринттиккет* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8f176-120">*ppPrintTicket* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f176-121">Адрес буфера, содержащего билет на печать, представляющий [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , переданный в *пдевмоде*.</span><span class="sxs-lookup"><span data-stu-id="8f176-121">The address of the buffer that contains a print ticket that represents the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passed in *pDevmode*.</span></span> <span data-ttu-id="8f176-122">Эта функция вызывает функцию [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) для выделения буфера.</span><span class="sxs-lookup"><span data-stu-id="8f176-122">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="8f176-123">Если буфер больше не нужен, вызывающий объект должен освободить его, вызвав [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="8f176-123">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="8f176-124">*пкбпринттиккетленгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8f176-124">*pcbPrintTicketLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f176-125">Размер билета печати (в байтах), возвращенного в *пппринттиккет*.</span><span class="sxs-lookup"><span data-stu-id="8f176-125">The size, in bytes, of the print ticket returned in *ppPrintTicket*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f176-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8f176-126">Return value</span></span>

<span data-ttu-id="8f176-127">Если метод завершается успешно, возвращается значение **\_ ОК**. в противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8f176-127">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="8f176-128">Дополнительные сведения о кодах ошибок COM см. в разделе [Обработка ошибок](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="8f176-128">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f176-129">Требования</span><span class="sxs-lookup"><span data-stu-id="8f176-129">Requirements</span></span>



| <span data-ttu-id="8f176-130">Требование</span><span class="sxs-lookup"><span data-stu-id="8f176-130">Requirement</span></span> | <span data-ttu-id="8f176-131">Значение</span><span class="sxs-lookup"><span data-stu-id="8f176-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f176-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8f176-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8f176-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8f176-133">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8f176-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8f176-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8f176-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8f176-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8f176-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8f176-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f176-137"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f176-137"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f176-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8f176-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f176-139">Схема печати</span><span class="sxs-lookup"><span data-stu-id="8f176-139">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="8f176-140">**птконвертдевмодетопринттиккет**</span><span class="sxs-lookup"><span data-stu-id="8f176-140">**PTConvertDevModeToPrintTicket**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)
</dt> <dt>

[<span data-ttu-id="8f176-141">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="8f176-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8f176-142">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="8f176-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

