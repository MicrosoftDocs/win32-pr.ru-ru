---
title: Метод Инапклиентманажемент Жетнапклиентинфо (Напманажемент. h)
description: Извлекает сведения о клиенте NAP.
ms.assetid: c0b57cab-729b-40b2-81d2-32a961e377a5
keywords:
- Метод Жетнапклиентинфо NAP
- Метод Жетнапклиентинфо NAP, интерфейс Инапклиентманажемент
- Инапклиентманажемент интерфейса NAP, метод Жетнапклиентинфо
topic_type:
- apiref
api_name:
- INapClientManagement.GetNapClientInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11fc496374f2a7f0b7842e22212013149f44f22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534631"
---
# <a name="inapclientmanagementgetnapclientinfo-method"></a><span data-ttu-id="708c3-106">Метод Инапклиентманажемент:: Жетнапклиентинфо</span><span class="sxs-lookup"><span data-stu-id="708c3-106">INapClientManagement::GetNapClientInfo method</span></span>

> [!Note]  
> <span data-ttu-id="708c3-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="708c3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="708c3-108">Метод **жетнапклиентинфо** извлекает сведения о клиенте NAP.</span><span class="sxs-lookup"><span data-stu-id="708c3-108">The **GetNapClientInfo** method retrieves information about the NAP client.</span></span>

## <a name="syntax"></a><span data-ttu-id="708c3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="708c3-109">Syntax</span></span>


```C++
HRESULT GetNapClientInfo(
  [out] BOOL          *isNapEnabled,
  [out] CountedString **clientName,
  [out] CountedString **clientDescription,
  [out] CountedString **protocolVersion
) const;
```



## <a name="parameters"></a><span data-ttu-id="708c3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="708c3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="708c3-111">*иснапенаблед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="708c3-111">*isNapEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="708c3-112">Указатель на логическое значение **true** , если включен NAP. в противном случае — значение **false**.</span><span class="sxs-lookup"><span data-stu-id="708c3-112">A pointer to a BOOL that is set to **TRUE** if NAP is enabled; otherwise it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="708c3-113">*clientName* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="708c3-113">*clientName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="708c3-114">Указатель на указатель на структуру [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) , содержащую имя клиента.</span><span class="sxs-lookup"><span data-stu-id="708c3-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the client name.</span></span>

</dd> <dt>

<span data-ttu-id="708c3-115">*клиентдескриптион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="708c3-115">*clientDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="708c3-116">Указатель на указатель на структуру [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) , содержащую описание клиента.</span><span class="sxs-lookup"><span data-stu-id="708c3-116">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the client description.</span></span>

</dd> <dt>

<span data-ttu-id="708c3-117">*протоколверсион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="708c3-117">*protocolVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="708c3-118">Указатель на указатель на структуру [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) , содержащую версию протокола.</span><span class="sxs-lookup"><span data-stu-id="708c3-118">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the protocol version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="708c3-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="708c3-119">Return value</span></span>

<span data-ttu-id="708c3-120">Метод возвращает код состояния HRESULT, включая, помимо прочего, один из следующих.</span><span class="sxs-lookup"><span data-stu-id="708c3-120">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="708c3-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="708c3-121">Return code</span></span>                                                                                         | <span data-ttu-id="708c3-122">Описание</span><span class="sxs-lookup"><span data-stu-id="708c3-122">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="708c3-123"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="708c3-123"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="708c3-124">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="708c3-124">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="708c3-125"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="708c3-125"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="708c3-126">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="708c3-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="708c3-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="708c3-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="708c3-128">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="708c3-128">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="708c3-129"><dt>**RPC \_ E \_ отключен**</dt></span><span class="sxs-lookup"><span data-stu-id="708c3-129"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="708c3-130">Напажент не работает.</span><span class="sxs-lookup"><span data-stu-id="708c3-130">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="708c3-131">Требования</span><span class="sxs-lookup"><span data-stu-id="708c3-131">Requirements</span></span>



| <span data-ttu-id="708c3-132">Требование</span><span class="sxs-lookup"><span data-stu-id="708c3-132">Requirement</span></span> | <span data-ttu-id="708c3-133">Значение</span><span class="sxs-lookup"><span data-stu-id="708c3-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="708c3-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="708c3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="708c3-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="708c3-135">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="708c3-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="708c3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="708c3-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="708c3-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="708c3-138">Header</span><span class="sxs-lookup"><span data-stu-id="708c3-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="708c3-139"><dt>Напманажемент. h</dt></span><span class="sxs-lookup"><span data-stu-id="708c3-139"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="708c3-140">IDL</span><span class="sxs-lookup"><span data-stu-id="708c3-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="708c3-141"><dt>Напманажемент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="708c3-141"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="708c3-142">DLL</span><span class="sxs-lookup"><span data-stu-id="708c3-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="708c3-143"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="708c3-143"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="708c3-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="708c3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="708c3-145">**инапклиентманажемент**</span><span class="sxs-lookup"><span data-stu-id="708c3-145">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





