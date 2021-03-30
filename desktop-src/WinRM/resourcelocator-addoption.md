---
title: ResourceLocator. Аддоптион, метод (Всмандисп. h)
description: Добавляет дополнительные данные, необходимые для обработки запроса. Например, некоторым поставщикам WMI может потребоваться объект Ивбемконтекст или Свбемнамедвалуесет с информацией, зависящей от поставщика.
ms.assetid: c85949fc-41e7-47eb-8aab-9b456490bc81
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Аддоптион
- Служба удаленного управления Windows метода Аддоптион, объект ResourceLocator
- Служба удаленного управления Windows объекта ResourceLocator, метод Аддоптион
topic_type:
- apiref
api_name:
- ResourceLocator.AddOption
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 882f400dd2c59d2395dd2755846245f4e4ad385e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071273"
---
# <a name="resourcelocatoraddoption-method"></a><span data-ttu-id="1b618-107">ResourceLocator. Аддоптион, метод</span><span class="sxs-lookup"><span data-stu-id="1b618-107">ResourceLocator.AddOption method</span></span>

<span data-ttu-id="1b618-108">Добавляет дополнительные данные, необходимые для обработки запроса.</span><span class="sxs-lookup"><span data-stu-id="1b618-108">Adds additional data required to process the request.</span></span> <span data-ttu-id="1b618-109">Например, некоторым поставщикам WMI может потребоваться объект [**ивбемконтекст**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) или [**свбемнамедвалуесет**](/windows/desktop/WmiSdk/swbemnamedvalueset) с информацией, зависящей от поставщика.</span><span class="sxs-lookup"><span data-stu-id="1b618-109">For example, some WMI providers may require an [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) or [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) object with provider-specific information.</span></span> <span data-ttu-id="1b618-110">Можно предоставить объект [**ResourceLocator**](resourcelocator.md) вместо указания URI ресурса в операциях объекта [**сеанса**](session.md) , таких как [**Session. Get**](session-get.md), [**Session.**](session-put.md)WHERE или [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="1b618-110">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1b618-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b618-111">Syntax</span></span>


```VB
ResourceLocator.AddOption( _
  ByVal OptionName, _
  ByVal OptionValue, _
  ByVal mustComply _
)
```



## <a name="parameters"></a><span data-ttu-id="1b618-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b618-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b618-113">*OptionName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b618-113">*OptionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b618-114">Имя (ключ) необязательного объекта данных.</span><span class="sxs-lookup"><span data-stu-id="1b618-114">The name (key) of the optional data object.</span></span>

</dd> <dt>

<span data-ttu-id="1b618-115">*OptionValue* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b618-115">*OptionValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b618-116">Значение, заданное для необязательного объекта данных.</span><span class="sxs-lookup"><span data-stu-id="1b618-116">A value supplied for the optional data object.</span></span>

</dd> <dt>

<span data-ttu-id="1b618-117">*мусткомпли* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b618-117">*mustComply* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b618-118">Флаг, указывающий, что параметр должен быть обработан.</span><span class="sxs-lookup"><span data-stu-id="1b618-118">A flag that indicates the option must be processed.</span></span> <span data-ttu-id="1b618-119">Значение по умолчанию — **false** (0).</span><span class="sxs-lookup"><span data-stu-id="1b618-119">The default is **False** (0).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b618-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1b618-120">Return value</span></span>

<span data-ttu-id="1b618-121">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1b618-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b618-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1b618-122">Remarks</span></span>

<span data-ttu-id="1b618-123">**Ивсманресаурцелокатор:: аддоптион** — соответствующий метод C++.</span><span class="sxs-lookup"><span data-stu-id="1b618-123">**IWSManResourceLocator::AddOption** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b618-124">Требования</span><span class="sxs-lookup"><span data-stu-id="1b618-124">Requirements</span></span>



| <span data-ttu-id="1b618-125">Требование</span><span class="sxs-lookup"><span data-stu-id="1b618-125">Requirement</span></span> | <span data-ttu-id="1b618-126">Значение</span><span class="sxs-lookup"><span data-stu-id="1b618-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b618-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1b618-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1b618-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b618-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="1b618-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1b618-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1b618-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b618-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="1b618-131">Header</span><span class="sxs-lookup"><span data-stu-id="1b618-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b618-132"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b618-132"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1b618-133">IDL</span><span class="sxs-lookup"><span data-stu-id="1b618-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1b618-134"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1b618-134"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="1b618-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1b618-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="1b618-136"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1b618-136"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1b618-137">DLL</span><span class="sxs-lookup"><span data-stu-id="1b618-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b618-138"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b618-138"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1b618-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b618-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b618-140">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="1b618-140">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

