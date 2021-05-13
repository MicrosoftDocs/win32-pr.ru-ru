---
description: Оценивает риск выполнения неизвестного кода при вызове обработчика для данного файла. Этот риск основан на понимании обработчика и содержимого кода файла.
title: Функция Естиматефилерисклевел
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EstimateFileRiskLevel
api_type:
- DllExport
api_location:
- Winshfhc.dll
ms.assetid: 33a5589a-201b-4d94-afbf-5965a39e2748
ms.openlocfilehash: 2def6cb5bc2ed59a98e9e513aba1b5b578cd8681
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841435"
---
# <a name="estimatefilerisklevel-function"></a><span data-ttu-id="591d3-104">Функция Естиматефилерисклевел</span><span class="sxs-lookup"><span data-stu-id="591d3-104">EstimateFileRiskLevel function</span></span>

<span data-ttu-id="591d3-105">\[Эта функция доступна в Windows XP с пакетом обновления 2 (SP2) и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="591d3-105">\[This function is available on Windows XP with Service Pack 2 (SP2) through Windows Vista.</span></span> <span data-ttu-id="591d3-106">Он может быть изменен или недоступен в последующих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="591d3-106">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="591d3-107">Вместо этого клиентские приложения должны использовать [**иаттачментексекуте**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) для предоставления среды пользователя, которая обеспечивает безопасность загрузки и обмена файлами по электронной почте и вложениям в сообщения.\]</span><span class="sxs-lookup"><span data-stu-id="591d3-107">Client applications instead should use [**IAttachmentExecute**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) to present a user environment that provides safe download and exchange of files through email and messaging attachments.\]</span></span>

<span data-ttu-id="591d3-108">Оценивает риск выполнения неизвестного кода при вызове обработчика для данного файла.</span><span class="sxs-lookup"><span data-stu-id="591d3-108">Estimates the risk of executing unknown code when a handler is called on a given file.</span></span> <span data-ttu-id="591d3-109">Этот риск основан на понимании обработчика и содержимого кода файла.</span><span class="sxs-lookup"><span data-stu-id="591d3-109">This risk is based on an understanding of the handler and the code content of the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="591d3-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="591d3-110">Syntax</span></span>


```C++
HRESULT EstimateFileRiskLevel(
  _In_  LPCWSTR         pszFilePath,
  _In_  LPCWSTR         pszExt,
  _In_  LPCWSTR         pszHandler,
  _Out_ FILE_RISK_LEVEL *pfrlEstimate
);
```



## <a name="parameters"></a><span data-ttu-id="591d3-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="591d3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="591d3-112">*псзфилепас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="591d3-112">*pszFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="591d3-113">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="591d3-113">Type: **LPCWSTR**</span></span>

<span data-ttu-id="591d3-114">Указатель на строку, завершающуюся нулем, которая содержит путь к файлу, проверяемому на соответствие обработчику.</span><span class="sxs-lookup"><span data-stu-id="591d3-114">A pointer to a null-terminated string that contains the path of the file that is being checked against the handler.</span></span>

</dd> <dt>

<span data-ttu-id="591d3-115">*псзекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="591d3-115">*pszExt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="591d3-116">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="591d3-116">Type: **LPCWSTR**</span></span>

<span data-ttu-id="591d3-117">Указатель на строку, завершающуюся нулем, которая содержит расширение проверяемого файла либо с предшествующей точкой, так и без нее.</span><span class="sxs-lookup"><span data-stu-id="591d3-117">A pointer to a null-terminated string that contains the extension of the file that is being checked, either with or without its leading period.</span></span> <span data-ttu-id="591d3-118">Например, ". txt" или "txt".</span><span class="sxs-lookup"><span data-stu-id="591d3-118">For instance, ".txt" or "txt".</span></span>

</dd> <dt>

<span data-ttu-id="591d3-119">*псзандлер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="591d3-119">*pszHandler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="591d3-120">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="591d3-120">Type: **LPCWSTR**</span></span>

<span data-ttu-id="591d3-121">Указатель на строку, завершающуюся нулем, которая содержит путь к обработчику для файла.</span><span class="sxs-lookup"><span data-stu-id="591d3-121">A pointer to a null-terminated string that contains the path of the handler for the file.</span></span>

</dd> <dt>

<span data-ttu-id="591d3-122">*пфрлестимате* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="591d3-122">*pfrlEstimate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="591d3-123">Тип: **\_ \_ уровень \* риска файла**</span><span class="sxs-lookup"><span data-stu-id="591d3-123">Type: **FILE\_RISK\_LEVEL\***</span></span>

<span data-ttu-id="591d3-124">При успешном возврате этой функции содержит указатель на одно из следующих значений, которые заменяют предполагаемый риск.</span><span class="sxs-lookup"><span data-stu-id="591d3-124">When this function returns successfully, contains a pointer to one of the following values that state the estimated risk.</span></span>

<dt>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>

<span data-ttu-id="591d3-125"><span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>**ФРЛ \_ НЕТ \_ мнения** (0)</span><span class="sxs-lookup"><span data-stu-id="591d3-125"><span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>**FRL\_NO\_OPINION** (0)</span></span>


</dt> <dd>

<span data-ttu-id="591d3-126">Формат файла не определен, или обработчик не определен.</span><span class="sxs-lookup"><span data-stu-id="591d3-126">The format of the file is not identified or the handler is not identified.</span></span> <span data-ttu-id="591d3-127">Недостаточно сведений для осмысленного ответа.</span><span class="sxs-lookup"><span data-stu-id="591d3-127">Insufficient information available for a meaningful answer.</span></span>

</dd> <dt>

<span id="FRL_LOW"></span><span id="frl_low"></span>

<span data-ttu-id="591d3-128"><span id="FRL_LOW"></span><span id="frl_low"></span>**ФРЛ \_ НИЗКАЯ** (1)</span><span class="sxs-lookup"><span data-stu-id="591d3-128"><span id="FRL_LOW"></span><span id="frl_low"></span>**FRL\_LOW** (1)</span></span>


</dt> <dd>

<span data-ttu-id="591d3-129">Формат файла полностью понятен, обработчик известен, и существует высокая уверенность в том, что лишний код не будет выполняться.</span><span class="sxs-lookup"><span data-stu-id="591d3-129">The format of the file is completely understood, the handler is known, and there is high confidence that no extraneous code will be executed.</span></span>

</dd> <dt>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>

<span data-ttu-id="591d3-130"><span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**ФРЛ \_ УМЕРЕНное** (2)</span><span class="sxs-lookup"><span data-stu-id="591d3-130"><span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**FRL\_MODERATE** (2)</span></span>


</dt> <dd>

<span data-ttu-id="591d3-131">Формат файла определен, но он не может быть понятен метке как высокий или низкий риск.</span><span class="sxs-lookup"><span data-stu-id="591d3-131">The format of the file is identified, but it is not sufficiently understood to label as either a high or low risk.</span></span>

</dd> <dt>

<span id="FRL_HIGH"></span><span id="frl_high"></span>

<span data-ttu-id="591d3-132"><span id="FRL_HIGH"></span><span id="frl_high"></span>**ФРЛ \_ ВЫСОКИЙ** (3)</span><span class="sxs-lookup"><span data-stu-id="591d3-132"><span id="FRL_HIGH"></span><span id="frl_high"></span>**FRL\_HIGH** (3)</span></span>


</dt> <dd>

<span data-ttu-id="591d3-133">Формат файла понятен, и были обнаружены повышенные факторы риска.</span><span class="sxs-lookup"><span data-stu-id="591d3-133">The file format is understood and elevated risk factors have been identified.</span></span>

</dd> <dt>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>

<span data-ttu-id="591d3-134"><span id="FRL_BLOCK"></span><span id="frl_block"></span>**ФРЛ \_ BLOCK** (4)</span><span class="sxs-lookup"><span data-stu-id="591d3-134"><span id="FRL_BLOCK"></span><span id="frl_block"></span>**FRL\_BLOCK** (4)</span></span>


</dt> <dd>

<span data-ttu-id="591d3-135">Формат файла специально заблокирован для этого обработчика.</span><span class="sxs-lookup"><span data-stu-id="591d3-135">The file format is specifically blocked for this handler.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="591d3-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="591d3-136">Return value</span></span>

<span data-ttu-id="591d3-137">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="591d3-137">Type: **HRESULT**</span></span>

<span data-ttu-id="591d3-138">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="591d3-138">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="591d3-139">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="591d3-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="591d3-140">Remarks</span><span class="sxs-lookup"><span data-stu-id="591d3-140">Remarks</span></span>

<span data-ttu-id="591d3-141">Эта функция не объявлена в общедоступном заголовке или включена в файл библиотеки.</span><span class="sxs-lookup"><span data-stu-id="591d3-141">This function is not declared in a public header or included in a library file.</span></span> <span data-ttu-id="591d3-142">Чтобы использовать его, необходимо загрузить его непосредственно из Winshfhc.dll с порядковым номером 101.</span><span class="sxs-lookup"><span data-stu-id="591d3-142">To use it you must load it directly from Winshfhc.dll by ordinal 101.</span></span>

## <a name="requirements"></a><span data-ttu-id="591d3-143">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="591d3-143">Requirements</span></span>



| <span data-ttu-id="591d3-144">Требование</span><span class="sxs-lookup"><span data-stu-id="591d3-144">Requirement</span></span> | <span data-ttu-id="591d3-145">Значение</span><span class="sxs-lookup"><span data-stu-id="591d3-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="591d3-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="591d3-146">Minimum supported client</span></span><br/> | <span data-ttu-id="591d3-147">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="591d3-147">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="591d3-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="591d3-148">Minimum supported server</span></span><br/> | <span data-ttu-id="591d3-149">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="591d3-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="591d3-150">DLL</span><span class="sxs-lookup"><span data-stu-id="591d3-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="591d3-151"><dt>Winshfhc.dll (версия 5,1 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="591d3-151"><dt>Winshfhc.dll (version 5.1 or later)</dt></span></span> </dl> |



 

 




