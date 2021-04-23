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
# <a name="getprintcapabilitiesthunk2-function"></a><span data-ttu-id="c7aa6-103">Функция GetPrintCapabilitiesThunk2</span><span class="sxs-lookup"><span data-stu-id="c7aa6-103">GetPrintCapabilitiesThunk2 function</span></span>

<span data-ttu-id="c7aa6-104">\[Эта функция не поддерживается и может быть отключена или удалена в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="c7aa6-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="c7aa6-105">[**Птжетпринткапабилитиес**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities) предоставляет эквивалентную функциональность, и вместо нее следует использовать.\]</span><span class="sxs-lookup"><span data-stu-id="c7aa6-105">[**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="c7aa6-106">Получает возможности принтера, отформатированные в соответствии с XML- [схемой печати](./printschema.md).</span><span class="sxs-lookup"><span data-stu-id="c7aa6-106">Retrieves the printer's capabilities formatted in compliance with the XML [Print Schema](./printschema.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c7aa6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7aa6-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="c7aa6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7aa6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7aa6-109">*хпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7aa6-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7aa6-110">Маркер открытого поставщика билетов на печать.</span><span class="sxs-lookup"><span data-stu-id="c7aa6-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="c7aa6-111">Этот маркер возвращается функцией [**биндптпровидерсунк**](bindptproviderthunk.md) .</span><span class="sxs-lookup"><span data-stu-id="c7aa6-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="c7aa6-112">*ппринттиккет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7aa6-112">*pPrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7aa6-113">Буфер, содержащий данные билета на печать, выраженные в формате XML, как описано в [схеме печати](./printschema.md).</span><span class="sxs-lookup"><span data-stu-id="c7aa6-113">The buffer that contains the print ticket data, expressed in XML as described in the [Print Schema](./printschema.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7aa6-114">*кбпринттиккет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7aa6-114">*cbPrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7aa6-115">Размер (в байтах) буфера, на который ссылается *ппринттиккет*.</span><span class="sxs-lookup"><span data-stu-id="c7aa6-115">The size, in bytes, of the buffer referenced by *pPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="c7aa6-116">*ппбпринткапабилитиес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c7aa6-116">*ppbPrintCapabilities* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7aa6-117">Адрес буфера, выделенный этой функцией и содержащий допустимые сведения о возможностях печати, закодированные как XML.</span><span class="sxs-lookup"><span data-stu-id="c7aa6-117">The address of the buffer that is allocated by this function and contains the valid print capabilities information, encoded as XML.</span></span> <span data-ttu-id="c7aa6-118">Эта функция вызывает функцию [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) для выделения буфера.</span><span class="sxs-lookup"><span data-stu-id="c7aa6-118">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="c7aa6-119">Если буфер больше не нужен, вызывающий объект должен освободить его, вызвав [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="c7aa6-119">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="c7aa6-120">*пкбпринткапабилитиесленгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c7aa6-120">*pcbPrintCapabilitiesLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7aa6-121">Размер (в байтах) буфера, на который ссылается *ппбпринткапабилитиес*.</span><span class="sxs-lookup"><span data-stu-id="c7aa6-121">The size, in bytes, of the buffer referenced by *ppbPrintCapabilities*.</span></span>

</dd> <dt>

<span data-ttu-id="c7aa6-122">*пбстреррормессаже* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="c7aa6-122">*pbstrErrorMessage* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c7aa6-123">Указатель на строку, указывающую, что, если что-либо является недопустимым для *ппринттиккет*.</span><span class="sxs-lookup"><span data-stu-id="c7aa6-123">A pointer to a string that specifies what, if anything, is invalid about *pPrintTicket*.</span></span> <span data-ttu-id="c7aa6-124">Если он является допустимым, это значение равно **null**.</span><span class="sxs-lookup"><span data-stu-id="c7aa6-124">If it is valid, this value is **NULL**.</span></span> <span data-ttu-id="c7aa6-125">Если *пбстреррормессаже* не **равно NULL** , то при возврате функции вызывающий объект должен освободить строку с помощью [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span><span class="sxs-lookup"><span data-stu-id="c7aa6-125">If *pbstrErrorMessage* is not **NULL** when the function returns, the caller must free the string with [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7aa6-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7aa6-126">Return value</span></span>

<span data-ttu-id="c7aa6-127">Если метод завершается успешно, возвращается значение **\_ ОК**. в противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c7aa6-127">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="c7aa6-128">Дополнительные сведения о кодах ошибок COM см. в разделе [Обработка ошибок](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="c7aa6-128">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7aa6-129">Требования</span><span class="sxs-lookup"><span data-stu-id="c7aa6-129">Requirements</span></span>



| <span data-ttu-id="c7aa6-130">Требование</span><span class="sxs-lookup"><span data-stu-id="c7aa6-130">Requirement</span></span> | <span data-ttu-id="c7aa6-131">Значение</span><span class="sxs-lookup"><span data-stu-id="c7aa6-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7aa6-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7aa6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c7aa6-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c7aa6-133">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c7aa6-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7aa6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c7aa6-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c7aa6-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c7aa6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c7aa6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7aa6-137"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7aa6-137"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7aa6-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7aa6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7aa6-139">**птжетпринткапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="c7aa6-139">**PTGetPrintCapabilities**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)
</dt> <dt>

[<span data-ttu-id="c7aa6-140">Схема печати</span><span class="sxs-lookup"><span data-stu-id="c7aa6-140">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="c7aa6-141">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="c7aa6-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c7aa6-142">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="c7aa6-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

