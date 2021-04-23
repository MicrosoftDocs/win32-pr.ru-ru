---
title: Метод Инапкомпонентконфиг Инвокеуи (Напкоммон. h)
description: Запускает настраиваемый пользовательский интерфейс для компонента средства проверки работоспособности системы (SHV).
ms.assetid: da2a5e3e-bc17-4984-bdbe-b72e9e710a9d
keywords:
- Метод Инвокеуи NAP
- Метод Инвокеуи NAP, интерфейс Инапкомпонентконфиг
- Инапкомпонентконфиг интерфейса NAP, метод Инвокеуи
topic_type:
- apiref
api_name:
- INapComponentConfig.InvokeUI
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd86d683365286fc2130c1ac9edf21ff075d61a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988451"
---
# <a name="inapcomponentconfiginvokeui-method"></a><span data-ttu-id="41936-106">Метод Инапкомпонентконфиг:: Инвокеуи</span><span class="sxs-lookup"><span data-stu-id="41936-106">INapComponentConfig::InvokeUI method</span></span>

> [!Note]  
> <span data-ttu-id="41936-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="41936-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="41936-108">Метод **инвокеуи** запускает настраиваемый пользовательский интерфейс для компонента средства проверки работоспособности системы (SHV).</span><span class="sxs-lookup"><span data-stu-id="41936-108">The **InvokeUI** method launches a customized user interface for a system health validator (SHV) component.</span></span>

## <a name="syntax"></a><span data-ttu-id="41936-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41936-109">Syntax</span></span>


```C++
HRESULT InvokeUI(
  [in] HWND hwndParent
) const;
```



## <a name="parameters"></a><span data-ttu-id="41936-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="41936-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41936-111">*хвндпарент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41936-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41936-112">Маркер родительского окна или окно-владельца.</span><span class="sxs-lookup"><span data-stu-id="41936-112">A handle to the parent or owner window.</span></span> <span data-ttu-id="41936-113">Необходимо указать допустимый описатель окна.</span><span class="sxs-lookup"><span data-stu-id="41936-113">A valid window handle must be supplied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41936-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41936-114">Return value</span></span>

<span data-ttu-id="41936-115">Возвращает один из следующих кодов ошибок в зависимости от результата этой операции.</span><span class="sxs-lookup"><span data-stu-id="41936-115">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="41936-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="41936-116">Return code</span></span>                                                                                     | <span data-ttu-id="41936-117">Описание</span><span class="sxs-lookup"><span data-stu-id="41936-117">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="41936-118"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="41936-118"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="41936-119">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="41936-119">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="41936-120"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="41936-120"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="41936-121">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="41936-121">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="41936-122"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="41936-122"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="41936-123">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="41936-123">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="41936-124"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="41936-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>       | <span data-ttu-id="41936-125">SHV не поддерживает настраиваемый пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="41936-125">The SHV does not support a customized UI.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="41936-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="41936-126">Remarks</span></span>

<span data-ttu-id="41936-127">Этот вызов метода должен блокироваться до тех пор, пока пользовательский интерфейс SHV не завершит работу.</span><span class="sxs-lookup"><span data-stu-id="41936-127">This method call should block until the SHV user interface exits.</span></span>

## <a name="requirements"></a><span data-ttu-id="41936-128">Требования</span><span class="sxs-lookup"><span data-stu-id="41936-128">Requirements</span></span>



| <span data-ttu-id="41936-129">Требование</span><span class="sxs-lookup"><span data-stu-id="41936-129">Requirement</span></span> | <span data-ttu-id="41936-130">Значение</span><span class="sxs-lookup"><span data-stu-id="41936-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="41936-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41936-131">Minimum supported client</span></span><br/> | <span data-ttu-id="41936-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="41936-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="41936-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41936-133">Minimum supported server</span></span><br/> | <span data-ttu-id="41936-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="41936-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="41936-135">Header</span><span class="sxs-lookup"><span data-stu-id="41936-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="41936-136"><dt>Напкоммон. h</dt></span><span class="sxs-lookup"><span data-stu-id="41936-136"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="41936-137">IDL</span><span class="sxs-lookup"><span data-stu-id="41936-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="41936-138"><dt>Напкоммон. idl</dt></span><span class="sxs-lookup"><span data-stu-id="41936-138"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41936-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41936-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41936-140">**инапкомпонентконфиг**</span><span class="sxs-lookup"><span data-stu-id="41936-140">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="41936-141">**Инапкомпонентконфиг:: Исуисуппортед**</span><span class="sxs-lookup"><span data-stu-id="41936-141">**INapComponentConfig::IsUISupported**</span></span>](inapcomponentconfig-isuisupported.md)
</dt> </dl>

 

 





