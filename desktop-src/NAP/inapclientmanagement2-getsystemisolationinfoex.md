---
title: Метод INapClientManagement2 Жетсистемисолатионинфоекс (Напманажемент. h)
description: Извлекает сведения о состоянии изоляции и расширенном состоянии изоляции Напклиент.
ms.assetid: 614bcf19-873e-4043-98b2-dcb152bae3e2
keywords:
- Метод Жетсистемисолатионинфоекс NAP
- Метод Жетсистемисолатионинфоекс NAP, интерфейс INapClientManagement2
- INapClientManagement2 интерфейса NAP, метод Жетсистемисолатионинфоекс
topic_type:
- apiref
api_name:
- INapClientManagement2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e75a6554ea7e55c3bebe35b797f888494a55627
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071422"
---
# <a name="inapclientmanagement2getsystemisolationinfoex-method"></a><span data-ttu-id="17524-106">Метод INapClientManagement2:: Жетсистемисолатионинфоекс</span><span class="sxs-lookup"><span data-stu-id="17524-106">INapClientManagement2::GetSystemIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="17524-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="17524-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="17524-108">Метод **жетсистемисолатионинфоекс** извлекает сведения о состоянии изоляции и расширенном состоянии изоляции напклиент.</span><span class="sxs-lookup"><span data-stu-id="17524-108">The **GetSystemIsolationInfoEx** method retrieves information about the isolation state and extended isolation state of the NapClient.</span></span>

## <a name="syntax"></a><span data-ttu-id="17524-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17524-109">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a><span data-ttu-id="17524-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="17524-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17524-111">*исолатионинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="17524-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17524-112">Указатель на указатель на структуру [**исолатионинфоекс**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) , содержащую сведения о состоянии изоляции.</span><span class="sxs-lookup"><span data-stu-id="17524-112">A pointer to a pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains isolation state information.</span></span>

</dd> <dt>

<span data-ttu-id="17524-113">*ункновнконнектионс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="17524-113">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17524-114">Указатель на логическое значение, равное **true** , если какое-либо из соединений находится в неизвестном состоянии, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="17524-114">A pointer to a BOOL that is **TRUE** if any of the connections are in an unknown state and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17524-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17524-115">Return value</span></span>

<span data-ttu-id="17524-116">Метод возвращает код состояния HRESULT, включая, помимо прочего, один из следующих.</span><span class="sxs-lookup"><span data-stu-id="17524-116">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="17524-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="17524-117">Return code</span></span>                                                                                         | <span data-ttu-id="17524-118">Описание</span><span class="sxs-lookup"><span data-stu-id="17524-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="17524-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="17524-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="17524-120">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="17524-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="17524-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="17524-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="17524-122">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="17524-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="17524-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="17524-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="17524-124">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="17524-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="17524-125"><dt>**RPC \_ E \_ отключен**</dt></span><span class="sxs-lookup"><span data-stu-id="17524-125"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="17524-126">Напажент не работает.</span><span class="sxs-lookup"><span data-stu-id="17524-126">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="17524-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17524-127">Remarks</span></span>

<span data-ttu-id="17524-128">Извлеченные сведения о изоляции не отображают неизвестные состояния.</span><span class="sxs-lookup"><span data-stu-id="17524-128">The isolation information that is retrieved does not reflect unknown states.</span></span>

<span data-ttu-id="17524-129">SHA должен освободить структуру [**исолатионинфоекс**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) , вызвав [**фриисолатионинфоекс**](freeisolationinfoex.md).</span><span class="sxs-lookup"><span data-stu-id="17524-129">The SHA must free the [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure by calling [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="17524-130">Требования</span><span class="sxs-lookup"><span data-stu-id="17524-130">Requirements</span></span>



| <span data-ttu-id="17524-131">Требование</span><span class="sxs-lookup"><span data-stu-id="17524-131">Requirement</span></span> | <span data-ttu-id="17524-132">Значение</span><span class="sxs-lookup"><span data-stu-id="17524-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="17524-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="17524-133">Minimum supported client</span></span><br/> | <span data-ttu-id="17524-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="17524-134">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="17524-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="17524-135">Minimum supported server</span></span><br/> | <span data-ttu-id="17524-136">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="17524-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="17524-137">Header</span><span class="sxs-lookup"><span data-stu-id="17524-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="17524-138"><dt>Напманажемент. h</dt></span><span class="sxs-lookup"><span data-stu-id="17524-138"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="17524-139">IDL</span><span class="sxs-lookup"><span data-stu-id="17524-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="17524-140"><dt>Напманажемент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="17524-140"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="17524-141">DLL</span><span class="sxs-lookup"><span data-stu-id="17524-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17524-142"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17524-142"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="17524-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17524-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17524-144">**INapClientManagement2**</span><span class="sxs-lookup"><span data-stu-id="17524-144">**INapClientManagement2**</span></span>](inapclientmanagement2.md)
</dt> </dl>

 

 





