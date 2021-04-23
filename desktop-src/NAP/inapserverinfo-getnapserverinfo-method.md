---
title: Метод Инапсерверинфо Жетнапсерверинфо (Напсерверманажемент. h)
description: Извлекает сведения о сервере NAP.
ms.assetid: 02f7ce40-3443-4263-86b2-4276cbc7b694
keywords:
- Метод Жетнапсерверинфо NAP
- Метод Жетнапсерверинфо NAP, интерфейс Инапсерверинфо
- Инапсерверинфо интерфейса NAP, метод Жетнапсерверинфо
topic_type:
- apiref
api_name:
- INapServerInfo.GetNapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b182b9e1a5c8d7974128b062fd284c5af3f060f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804066"
---
# <a name="inapserverinfogetnapserverinfo-method"></a><span data-ttu-id="893d7-106">Метод Инапсерверинфо:: Жетнапсерверинфо</span><span class="sxs-lookup"><span data-stu-id="893d7-106">INapServerInfo::GetNapServerInfo method</span></span>

> [!Note]  
> <span data-ttu-id="893d7-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="893d7-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="893d7-108">Метод **инапсерверинфо:: жетнапсерверинфо** извлекает сведения о сервере NAP.</span><span class="sxs-lookup"><span data-stu-id="893d7-108">The **INapServerInfo::GetNapServerInfo** method retrieves information about the NAP server.</span></span>

## <a name="syntax"></a><span data-ttu-id="893d7-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="893d7-109">Syntax</span></span>


```C++
HRESULT GetNapServerInfo(
  [out] CountedString **serverName,
  [out] CountedString **serverDescription,
  [out] CountedString **protocolVersion
);
```



## <a name="parameters"></a><span data-ttu-id="893d7-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="893d7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="893d7-111">*имя сервера* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="893d7-111">*serverName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="893d7-112">Указатель на указатель на структуру [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) , содержащую имя сервера.</span><span class="sxs-lookup"><span data-stu-id="893d7-112">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the server name.</span></span>

</dd> <dt>

<span data-ttu-id="893d7-113">*Описание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="893d7-113">*serverDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="893d7-114">Указатель на указатель на структуру [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) , содержащую описание сервера.</span><span class="sxs-lookup"><span data-stu-id="893d7-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the server description.</span></span>

</dd> <dt>

<span data-ttu-id="893d7-115">*протоколверсион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="893d7-115">*protocolVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="893d7-116">Указатель на указатель на структуру [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) , содержащую версию протокола.</span><span class="sxs-lookup"><span data-stu-id="893d7-116">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the protocol version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="893d7-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="893d7-117">Return value</span></span>

<span data-ttu-id="893d7-118">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="893d7-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="893d7-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="893d7-119">Return code</span></span>                                                                                     | <span data-ttu-id="893d7-120">Описание</span><span class="sxs-lookup"><span data-stu-id="893d7-120">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="893d7-121"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="893d7-121"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="893d7-122">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="893d7-122">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="893d7-123"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="893d7-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="893d7-124">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="893d7-124">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="893d7-125"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="893d7-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="893d7-126">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="893d7-126">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="893d7-127">Требования</span><span class="sxs-lookup"><span data-stu-id="893d7-127">Requirements</span></span>



| <span data-ttu-id="893d7-128">Требование</span><span class="sxs-lookup"><span data-stu-id="893d7-128">Requirement</span></span> | <span data-ttu-id="893d7-129">Значение</span><span class="sxs-lookup"><span data-stu-id="893d7-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="893d7-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="893d7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="893d7-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="893d7-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="893d7-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="893d7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="893d7-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="893d7-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="893d7-134">Header</span><span class="sxs-lookup"><span data-stu-id="893d7-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="893d7-135"><dt>Напсерверманажемент. h</dt></span><span class="sxs-lookup"><span data-stu-id="893d7-135"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="893d7-136">IDL</span><span class="sxs-lookup"><span data-stu-id="893d7-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="893d7-137"><dt>Напсерверманажемент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="893d7-137"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="893d7-138">DLL</span><span class="sxs-lookup"><span data-stu-id="893d7-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="893d7-139"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="893d7-139"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="893d7-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="893d7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="893d7-141">**инапсерверинфо**</span><span class="sxs-lookup"><span data-stu-id="893d7-141">**INapServerInfo**</span></span>](inapserverinfo.md)
</dt> <dt>

[<span data-ttu-id="893d7-142">**каунтедстринг**</span><span class="sxs-lookup"><span data-stu-id="893d7-142">**CountedString**</span></span>](/windows/win32/api/naptypes/ns-naptypes-countedstring)
</dt> </dl>

 

 





