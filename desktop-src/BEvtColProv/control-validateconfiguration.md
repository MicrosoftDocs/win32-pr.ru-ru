---
description: Проверьте правильность текста конфигурации, не настроив его как активный. Возвращает 1 при успешном выполнении, 0 при ошибке.
ms.assetid: baeabed0-7717-498a-9886-e49e4a101711
ms.tgt_platform: multiple
title: Метод Валидатеконфигуратион класса Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ValidateConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: d4e1d0061b779a54973aeea1a487d8838781cf6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990344"
---
# <a name="validateconfiguration-method-of-the-control-class"></a><span data-ttu-id="2a24a-104">Метод Валидатеконфигуратион класса Control</span><span class="sxs-lookup"><span data-stu-id="2a24a-104">ValidateConfiguration method of the Control class</span></span>

<span data-ttu-id="2a24a-105">Проверьте правильность текста конфигурации, не настроив его как активный.</span><span class="sxs-lookup"><span data-stu-id="2a24a-105">Validate a configuration text for correctness without setting it active.</span></span> <span data-ttu-id="2a24a-106">Возвращает 1 при успешном выполнении, 0 при ошибке.</span><span class="sxs-lookup"><span data-stu-id="2a24a-106">Returns 1 on success, 0 on error.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a24a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a24a-107">Syntax</span></span>


```mof
Uint32 ValidateConfiguration(
  [in]  string Config,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="2a24a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a24a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a24a-109">*Конфигурация* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2a24a-109">*Config* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a24a-110">Проверяемая конфигурация.</span><span class="sxs-lookup"><span data-stu-id="2a24a-110">The configuration to check.</span></span>

</dd> <dt>

<span data-ttu-id="2a24a-111">*ErrorString* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2a24a-111">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a24a-112">Когда этот метод возвращает значение, если произошла ошибка, этот параметр содержит описание ошибки проверки для операции.</span><span class="sxs-lookup"><span data-stu-id="2a24a-112">When this method returns, if there was a error, this parameter contains a description of the validation error for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2a24a-113">*Варнингстринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2a24a-113">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a24a-114">При возврате из этого метода этот параметр содержит описание любых предупреждений проверки для операции.</span><span class="sxs-lookup"><span data-stu-id="2a24a-114">When this method returns, this parameter contains a description of any validation warnings for the operation.</span></span>

<span data-ttu-id="2a24a-115">Текстовая строка с предупреждениями.</span><span class="sxs-lookup"><span data-stu-id="2a24a-115">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="2a24a-116">*Инфостринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2a24a-116">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a24a-117">При возврате из этого метода этот параметр содержит набор сведений о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2a24a-117">When this method returns, this parameter contains a set of information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="2a24a-118">*ErrorType* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2a24a-118">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a24a-119">Если этот метод возвращает значение, если произошла ошибка проверки, этот параметр указывает тип ошибки.</span><span class="sxs-lookup"><span data-stu-id="2a24a-119">When this method returns, if there was a validation error, this parameter indicates the error type.</span></span>

<span data-ttu-id="2a24a-120">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="2a24a-120">The possible values are:</span></span>

<dt>

<span data-ttu-id="2a24a-121">0</span><span class="sxs-lookup"><span data-stu-id="2a24a-121">0</span></span>
</dt> <dd>

<span data-ttu-id="2a24a-122">Отсутствует аргумент.</span><span class="sxs-lookup"><span data-stu-id="2a24a-122">The argument is missing.</span></span>

</dd> <dt>

<span data-ttu-id="2a24a-123">1</span><span class="sxs-lookup"><span data-stu-id="2a24a-123">1</span></span>
</dt> <dd>

<span data-ttu-id="2a24a-124">Недопустимый формат аргумента.</span><span class="sxs-lookup"><span data-stu-id="2a24a-124">The argument format is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="2a24a-125">2</span><span class="sxs-lookup"><span data-stu-id="2a24a-125">2</span></span>
</dt> <dd>

<span data-ttu-id="2a24a-126">Недопустимый аргумент конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2a24a-126">A configuration argument is invalid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a24a-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a24a-127">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="2a24a-128">0</span><span class="sxs-lookup"><span data-stu-id="2a24a-128">0</span></span>

<span data-ttu-id="2a24a-129">Сбой</span><span class="sxs-lookup"><span data-stu-id="2a24a-129">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2a24a-130">1</span><span class="sxs-lookup"><span data-stu-id="2a24a-130">1</span></span>

<span data-ttu-id="2a24a-131">Успешно</span><span class="sxs-lookup"><span data-stu-id="2a24a-131">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2a24a-132">Требования</span><span class="sxs-lookup"><span data-stu-id="2a24a-132">Requirements</span></span>



| <span data-ttu-id="2a24a-133">Требование</span><span class="sxs-lookup"><span data-stu-id="2a24a-133">Requirement</span></span> | <span data-ttu-id="2a24a-134">Значение</span><span class="sxs-lookup"><span data-stu-id="2a24a-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a24a-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2a24a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2a24a-136">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2a24a-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2a24a-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2a24a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2a24a-138">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2a24a-138">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="2a24a-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2a24a-139">Namespace</span></span><br/>                | <span data-ttu-id="2a24a-140">Корневой \\ узел Microsoft \\ Windows \\ бутевентколлектор</span><span class="sxs-lookup"><span data-stu-id="2a24a-140">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="2a24a-141">MOF</span><span class="sxs-lookup"><span data-stu-id="2a24a-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a24a-142"><dt>Бутевентколлекторвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a24a-142"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a24a-143">DLL</span><span class="sxs-lookup"><span data-stu-id="2a24a-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a24a-144"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2a24a-144"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="2a24a-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a24a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a24a-146">**Элемента**</span><span class="sxs-lookup"><span data-stu-id="2a24a-146">**Control**</span></span>](control.md)
</dt> </dl>

 

 




