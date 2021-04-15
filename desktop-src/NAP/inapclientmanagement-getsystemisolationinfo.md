---
title: Метод Инапклиентманажемент Жетсистемисолатионинфо (Напманажемент. h)
description: Извлекает сведения о состоянии изоляции Напклиент.
ms.assetid: e1f69e66-71ca-402e-9c94-8af159d00b21
keywords:
- Метод Жетсистемисолатионинфо NAP
- Метод Жетсистемисолатионинфо NAP, интерфейс Инапклиентманажемент
- Инапклиентманажемент интерфейса NAP, метод Жетсистемисолатионинфо
topic_type:
- apiref
api_name:
- INapClientManagement.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b3d446e0a8068353be6656c16f0e6796df8922
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415892"
---
# <a name="inapclientmanagementgetsystemisolationinfo-method"></a><span data-ttu-id="b36f3-106">Метод Инапклиентманажемент:: Жетсистемисолатионинфо</span><span class="sxs-lookup"><span data-stu-id="b36f3-106">INapClientManagement::GetSystemIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="b36f3-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="b36f3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b36f3-108">Метод **жетсистемисолатионинфо** извлекает сведения о состоянии изоляции напклиент.</span><span class="sxs-lookup"><span data-stu-id="b36f3-108">The **GetSystemIsolationInfo** method retrieves information about the isolation state of the NapClient.</span></span>

## <a name="syntax"></a><span data-ttu-id="b36f3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b36f3-109">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
) const;
```



## <a name="parameters"></a><span data-ttu-id="b36f3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b36f3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b36f3-111">*исолатионинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b36f3-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b36f3-112">Указатель на указатель на структуру [**исолатионинфо**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) , содержащую сведения о состоянии изоляции.</span><span class="sxs-lookup"><span data-stu-id="b36f3-112">A pointer to a pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains isolation state information.</span></span>

</dd> <dt>

<span data-ttu-id="b36f3-113">*ункновнконнектионс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b36f3-113">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b36f3-114">Указатель на флаг, указывающий, что какое-либо из соединений находится в неизвестном состоянии.</span><span class="sxs-lookup"><span data-stu-id="b36f3-114">A pointer to a flag that indicates whether any of the connections are in an unknown state.</span></span> <span data-ttu-id="b36f3-115">Если какой-либо из них имеет значение, флаг принимает значение **true**; в противном случае для флага задается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="b36f3-115">If any of them are, the flag is set to **TRUE**; otherwise the flag is set to **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b36f3-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b36f3-116">Return value</span></span>

<span data-ttu-id="b36f3-117">Метод возвращает код состояния HRESULT, включая, помимо прочего, один из следующих.</span><span class="sxs-lookup"><span data-stu-id="b36f3-117">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="b36f3-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b36f3-118">Return code</span></span>                                                                                         | <span data-ttu-id="b36f3-119">Описание</span><span class="sxs-lookup"><span data-stu-id="b36f3-119">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b36f3-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b36f3-120"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="b36f3-121">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b36f3-121">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="b36f3-122"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="b36f3-122"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="b36f3-123">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="b36f3-123">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="b36f3-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b36f3-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="b36f3-125">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b36f3-125">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="b36f3-126"><dt>**RPC \_ E \_ отключен**</dt></span><span class="sxs-lookup"><span data-stu-id="b36f3-126"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="b36f3-127">Напажент не работает.</span><span class="sxs-lookup"><span data-stu-id="b36f3-127">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="b36f3-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b36f3-128">Remarks</span></span>

<span data-ttu-id="b36f3-129">Извлеченные сведения о изоляции не отображают неизвестные состояния.</span><span class="sxs-lookup"><span data-stu-id="b36f3-129">The isolation information that is retrieved does not reflect unknown states.</span></span>

## <a name="requirements"></a><span data-ttu-id="b36f3-130">Требования</span><span class="sxs-lookup"><span data-stu-id="b36f3-130">Requirements</span></span>



| <span data-ttu-id="b36f3-131">Требование</span><span class="sxs-lookup"><span data-stu-id="b36f3-131">Requirement</span></span> | <span data-ttu-id="b36f3-132">Значение</span><span class="sxs-lookup"><span data-stu-id="b36f3-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b36f3-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b36f3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b36f3-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b36f3-134">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b36f3-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b36f3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b36f3-136">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b36f3-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b36f3-137">Header</span><span class="sxs-lookup"><span data-stu-id="b36f3-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="b36f3-138"><dt>Напманажемент. h</dt></span><span class="sxs-lookup"><span data-stu-id="b36f3-138"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="b36f3-139">IDL</span><span class="sxs-lookup"><span data-stu-id="b36f3-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b36f3-140"><dt>Напманажемент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b36f3-140"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="b36f3-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b36f3-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b36f3-142"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b36f3-142"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="b36f3-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b36f3-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b36f3-144">**инапклиентманажемент**</span><span class="sxs-lookup"><span data-stu-id="b36f3-144">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





