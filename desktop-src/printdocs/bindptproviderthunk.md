---
description: Открывает экземпляр поставщика билетов на печать.
ms.assetid: 815cc360-8dcd-4c58-a64d-5d77436a8623
title: Функция Биндптпровидерсунк
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: bf63fc6faf9d47993fafb97c8d3a1c18d6d6c985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264343"
---
# <a name="bindptproviderthunk-function"></a><span data-ttu-id="6b77d-103">Функция Биндптпровидерсунк</span><span class="sxs-lookup"><span data-stu-id="6b77d-103">BindPTProviderThunk function</span></span>

<span data-ttu-id="6b77d-104">\[Эта функция не поддерживается и может быть отключена или удалена в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="6b77d-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="6b77d-105">[**Птопенпровидерекс**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex) предоставляет эквивалентную функциональность, и вместо нее следует использовать.\]</span><span class="sxs-lookup"><span data-stu-id="6b77d-105">[**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="6b77d-106">Открывает экземпляр поставщика билетов на печать.</span><span class="sxs-lookup"><span data-stu-id="6b77d-106">Opens an instance of a print ticket provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b77d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b77d-107">Syntax</span></span>


```C++
HRESULT BindPTProviderThunk(
  _In_  LPTSTR      pszPrinterName,
  _In_  INT         maxVersion,
  _In_  INT         prefVersion,
  _Out_ HPTPROVIDER *phProvider,
  _Out_ INT         *usedVersion
);
```



## <a name="parameters"></a><span data-ttu-id="6b77d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b77d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b77d-109">*псзпринтернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6b77d-109">*pszPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b77d-110">Полное имя очереди печати.</span><span class="sxs-lookup"><span data-stu-id="6b77d-110">The full name of a print queue.</span></span>

</dd> <dt>

<span data-ttu-id="6b77d-111">*maxVersion* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6b77d-111">*maxVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b77d-112">Последняя версия [схемы печати](./printschema.md) , которую поддерживает вызывающий объект.</span><span class="sxs-lookup"><span data-stu-id="6b77d-112">The latest version of the [Print Schema](./printschema.md) that the caller supports.</span></span>

</dd> <dt>

<span data-ttu-id="6b77d-113">*префверсион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6b77d-113">*prefVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b77d-114">Версия [схемы печати](./printschema.md) , запрошенная вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="6b77d-114">The version of the [Print Schema](./printschema.md) requested by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="6b77d-115">*фпровидер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6b77d-115">*phProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b77d-116">Указатель на маркер поставщика билетов на печать.</span><span class="sxs-lookup"><span data-stu-id="6b77d-116">A pointer to a handle to the print ticket provider.</span></span>

</dd> <dt>

<span data-ttu-id="6b77d-117">*уседверсион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6b77d-117">*usedVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b77d-118">Версия [схемы печати](./printschema.md) , которую будет использовать поставщик билетов на печать.</span><span class="sxs-lookup"><span data-stu-id="6b77d-118">The version of the [Print Schema](./printschema.md) that the print ticket provider will use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b77d-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b77d-119">Return value</span></span>

<span data-ttu-id="6b77d-120">Если метод завершается успешно, возвращается значение **\_ ОК**. в противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6b77d-120">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="6b77d-121">Дополнительные сведения о кодах ошибок COM см. в разделе [Обработка ошибок](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="6b77d-121">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6b77d-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6b77d-122">Remarks</span></span>

<span data-ttu-id="6b77d-123">Перед вызовом этой функции вызывающий поток должен инициализировать COM, вызвав [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="6b77d-123">Before calling this function, the calling thread must initialize COM by calling [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b77d-124">Требования</span><span class="sxs-lookup"><span data-stu-id="6b77d-124">Requirements</span></span>



| <span data-ttu-id="6b77d-125">Требование</span><span class="sxs-lookup"><span data-stu-id="6b77d-125">Requirement</span></span> | <span data-ttu-id="6b77d-126">Значение</span><span class="sxs-lookup"><span data-stu-id="6b77d-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b77d-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b77d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6b77d-128">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6b77d-128">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6b77d-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b77d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6b77d-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6b77d-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6b77d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="6b77d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b77d-132"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b77d-132"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b77d-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b77d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b77d-134">Схема печати</span><span class="sxs-lookup"><span data-stu-id="6b77d-134">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="6b77d-135">**птопенпровидерекс**</span><span class="sxs-lookup"><span data-stu-id="6b77d-135">**PTOpenProviderEx**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)
</dt> <dt>

[<span data-ttu-id="6b77d-136">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="6b77d-136">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6b77d-137">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="6b77d-137">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

