---
title: Метод Инапкомпонентконфиг Исуисуппортед (Напкоммон. h)
description: Указывает, поддерживает ли компонент настраиваемый пользовательский интерфейс.
ms.assetid: 044f8014-f041-4e9c-922a-2691b799ba84
keywords:
- Метод Исуисуппортед NAP
- Метод Исуисуппортед NAP, интерфейс Инапкомпонентконфиг
- Инапкомпонентконфиг интерфейса NAP, метод Исуисуппортед
topic_type:
- apiref
api_name:
- INapComponentConfig.IsUISupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab7d3f6b87ba5e483b466e6746f0f63d039cb205
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672653"
---
# <a name="inapcomponentconfigisuisupported-method"></a><span data-ttu-id="13647-106">Метод Инапкомпонентконфиг:: Исуисуппортед</span><span class="sxs-lookup"><span data-stu-id="13647-106">INapComponentConfig::IsUISupported method</span></span>

> [!Note]  
> <span data-ttu-id="13647-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="13647-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="13647-108">Метод **исуисуппортед** указывает, поддерживает ли компонент настраиваемый пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="13647-108">The **IsUISupported** method specifies whether the component supports a customized user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="13647-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13647-109">Syntax</span></span>


```C++
HRESULT IsUISupported(
  [out] BOOL *isSupported
) const;
```



## <a name="parameters"></a><span data-ttu-id="13647-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="13647-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13647-111">*поддерживается* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="13647-111">*isSupported* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13647-112">Указатель на логическое значение **true** , если компонент поддерживает настраиваемый пользовательский интерфейс, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="13647-112">A pointer to a BOOL that is set to **TRUE** if the component supports a customized user interface and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13647-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13647-113">Return value</span></span>

<span data-ttu-id="13647-114">Возвращает один из следующих кодов ошибок в зависимости от результата этой операции.</span><span class="sxs-lookup"><span data-stu-id="13647-114">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="13647-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="13647-115">Return code</span></span>                                                                                     | <span data-ttu-id="13647-116">Описание</span><span class="sxs-lookup"><span data-stu-id="13647-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="13647-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="13647-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="13647-118">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="13647-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="13647-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="13647-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="13647-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="13647-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="13647-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="13647-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="13647-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13647-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="13647-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="13647-123">Remarks</span></span>

<span data-ttu-id="13647-124">Настраиваемый пользовательский интерфейс компонента следует запускать с помощью [**инапкомпонентконфиг:: инвокеуи**](inapcomponentconfig-invokeui.md).</span><span class="sxs-lookup"><span data-stu-id="13647-124">A component's customized user interface should be launched using [**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="13647-125">Требования</span><span class="sxs-lookup"><span data-stu-id="13647-125">Requirements</span></span>



| <span data-ttu-id="13647-126">Требование</span><span class="sxs-lookup"><span data-stu-id="13647-126">Requirement</span></span> | <span data-ttu-id="13647-127">Значение</span><span class="sxs-lookup"><span data-stu-id="13647-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="13647-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13647-128">Minimum supported client</span></span><br/> | <span data-ttu-id="13647-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="13647-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="13647-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13647-130">Minimum supported server</span></span><br/> | <span data-ttu-id="13647-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="13647-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="13647-132">Header</span><span class="sxs-lookup"><span data-stu-id="13647-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="13647-133"><dt>Напкоммон. h</dt></span><span class="sxs-lookup"><span data-stu-id="13647-133"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="13647-134">IDL</span><span class="sxs-lookup"><span data-stu-id="13647-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="13647-135"><dt>Напкоммон. idl</dt></span><span class="sxs-lookup"><span data-stu-id="13647-135"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13647-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13647-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13647-137">**инапкомпонентконфиг**</span><span class="sxs-lookup"><span data-stu-id="13647-137">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="13647-138">**Инапкомпонентконфиг:: Инвокеуи**</span><span class="sxs-lookup"><span data-stu-id="13647-138">**INapComponentConfig::InvokeUI**</span></span>](inapcomponentconfig-invokeui.md)
</dt> </dl>

 

 





