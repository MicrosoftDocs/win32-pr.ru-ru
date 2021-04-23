---
title: Метод Инапсохпроцессор Жетнумберофаттрибутес (Наппротокол. h)
description: Возвращает общее число атрибутов в состоянии работоспособности.
ms.assetid: ee0b1857-65a7-47bb-ae91-c939344a24d0
keywords:
- Метод Жетнумберофаттрибутес NAP
- Метод Жетнумберофаттрибутес NAP, интерфейс Инапсохпроцессор
- Инапсохпроцессор интерфейса NAP, метод Жетнумберофаттрибутес
topic_type:
- apiref
api_name:
- INapSoHProcessor.GetNumberOfAttributes
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f1336362b44d49c71ce81b197f9f95b1a1b8fc9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534157"
---
# <a name="inapsohprocessorgetnumberofattributes-method"></a><span data-ttu-id="6ddf6-106">Метод Инапсохпроцессор:: Жетнумберофаттрибутес</span><span class="sxs-lookup"><span data-stu-id="6ddf6-106">INapSoHProcessor::GetNumberOfAttributes method</span></span>

> [!Note]  
> <span data-ttu-id="6ddf6-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="6ddf6-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6ddf6-108">Метод **инапсохпроцессор:: жетнумберофаттрибутес** получает общее количество атрибутов в состоянии работоспособности.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-108">The **INapSoHProcessor::GetNumberOfAttributes** method retrieves the total number of attributes in the SoH.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ddf6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ddf6-109">Syntax</span></span>


```C++
HRESULT GetNumberOfAttributes(
  [out] UINT16 *attributeCount
);
```



## <a name="parameters"></a><span data-ttu-id="6ddf6-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ddf6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ddf6-111">*аттрибутекаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6ddf6-111">*attributeCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ddf6-112">Указатель на возвращаемое число атрибутов.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-112">A pointer to the returned attribute count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ddf6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ddf6-113">Return value</span></span>

<span data-ttu-id="6ddf6-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="6ddf6-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6ddf6-115">Return code</span></span>                                                                                     | <span data-ttu-id="6ddf6-116">Описание</span><span class="sxs-lookup"><span data-stu-id="6ddf6-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="6ddf6-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="6ddf6-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="6ddf6-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="6ddf6-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="6ddf6-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="6ddf6-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="6ddf6-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6ddf6-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="6ddf6-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6ddf6-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6ddf6-123">Требования</span><span class="sxs-lookup"><span data-stu-id="6ddf6-123">Requirements</span></span>



| <span data-ttu-id="6ddf6-124">Требование</span><span class="sxs-lookup"><span data-stu-id="6ddf6-124">Requirement</span></span> | <span data-ttu-id="6ddf6-125">Значение</span><span class="sxs-lookup"><span data-stu-id="6ddf6-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ddf6-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ddf6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6ddf6-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6ddf6-127">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6ddf6-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ddf6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6ddf6-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6ddf6-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6ddf6-130">Header</span><span class="sxs-lookup"><span data-stu-id="6ddf6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ddf6-131"><dt>Наппротокол. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ddf6-131"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ddf6-132">IDL</span><span class="sxs-lookup"><span data-stu-id="6ddf6-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6ddf6-133"><dt>Наппротокол. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6ddf6-133"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="6ddf6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="6ddf6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ddf6-135"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ddf6-135"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="6ddf6-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ddf6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ddf6-137">**инапсохпроцессор**</span><span class="sxs-lookup"><span data-stu-id="6ddf6-137">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





