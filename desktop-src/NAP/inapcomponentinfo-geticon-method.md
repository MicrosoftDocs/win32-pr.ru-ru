---
title: Метод Инапкомпонентинфо-Icon (Напкоммон. h)
description: Используется системой защиты доступа к сети для получения значка клиента работоспособности.
ms.assetid: 6501fe12-1ec0-43a1-b672-b6cfd9a08d85
keywords:
- Метод Icon NAP
- Метод Icon NAP, интерфейс Инапкомпонентинфо
- Инапкомпонентинфо интерфейса NAP, метод method
topic_type:
- apiref
api_name:
- INapComponentInfo.GetIcon
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 795ad85f8497262f88fa55d8efb2da7466b8c3a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989270"
---
# <a name="inapcomponentinfogeticon-method"></a><span data-ttu-id="44e37-106">Инапкомпонентинфо:: метод Icon</span><span class="sxs-lookup"><span data-stu-id="44e37-106">INapComponentInfo::GetIcon method</span></span>

> [!Note]  
> <span data-ttu-id="44e37-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="44e37-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="44e37-108">Метод обратного вызова **инапкомпонентинфо::-Icon** используется системой защиты доступа к сети для получения значка клиента работоспособности.</span><span class="sxs-lookup"><span data-stu-id="44e37-108">The **INapComponentInfo::GetIcon** callback method is used by the NAP System to get the icon of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="44e37-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44e37-109">Syntax</span></span>


```C++
HRESULT GetIcon(
  [out] CountedString **dllFilePath,
  [out] UINT32        *iconResourceId
);
```



## <a name="parameters"></a><span data-ttu-id="44e37-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="44e37-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44e37-111">*дллфилепас* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="44e37-111">*dllFilePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44e37-112">Указатель на указатель на [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) , используемый для получения пути к файлу DLL, содержащему значок.</span><span class="sxs-lookup"><span data-stu-id="44e37-112">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) used to return the file path of the DLL that contains the icon.</span></span>

</dd> <dt>

<span data-ttu-id="44e37-113">*иконресаурцеид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="44e37-113">*iconResourceId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44e37-114">Указатель на значение, используемое для возврата идентификатора ресурса используемого значка.</span><span class="sxs-lookup"><span data-stu-id="44e37-114">A pointer to value used to return the resource ID of the icon to be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44e37-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44e37-115">Return value</span></span>

<span data-ttu-id="44e37-116">Возвращает один из этих кодов ошибок в зависимости от результата этой операции.</span><span class="sxs-lookup"><span data-stu-id="44e37-116">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="44e37-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="44e37-117">Return code</span></span>                                                                                     | <span data-ttu-id="44e37-118">Описание</span><span class="sxs-lookup"><span data-stu-id="44e37-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="44e37-119"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="44e37-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="44e37-120">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="44e37-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="44e37-121"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="44e37-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="44e37-122">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="44e37-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="44e37-123"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="44e37-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="44e37-124">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="44e37-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="44e37-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44e37-125">Remarks</span></span>

<span data-ttu-id="44e37-126">Значки должны быть локализованы в соответствии с идентификатором языка вызывающего потока.</span><span class="sxs-lookup"><span data-stu-id="44e37-126">Icons should be localized according to the calling thread's language-id.</span></span>

## <a name="requirements"></a><span data-ttu-id="44e37-127">Требования</span><span class="sxs-lookup"><span data-stu-id="44e37-127">Requirements</span></span>



| <span data-ttu-id="44e37-128">Требование</span><span class="sxs-lookup"><span data-stu-id="44e37-128">Requirement</span></span> | <span data-ttu-id="44e37-129">Значение</span><span class="sxs-lookup"><span data-stu-id="44e37-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="44e37-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="44e37-130">Minimum supported client</span></span><br/> | <span data-ttu-id="44e37-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="44e37-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="44e37-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="44e37-132">Minimum supported server</span></span><br/> | <span data-ttu-id="44e37-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="44e37-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="44e37-134">Header</span><span class="sxs-lookup"><span data-stu-id="44e37-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="44e37-135"><dt>Напкоммон. h</dt></span><span class="sxs-lookup"><span data-stu-id="44e37-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="44e37-136">IDL</span><span class="sxs-lookup"><span data-stu-id="44e37-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="44e37-137"><dt>Напкоммон. idl</dt></span><span class="sxs-lookup"><span data-stu-id="44e37-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44e37-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44e37-138">See also</span></span>

<dl> <span data-ttu-id="44e37-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="44e37-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="44e37-140">**инапкомпонентинфо**</span><span class="sxs-lookup"><span data-stu-id="44e37-140">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





