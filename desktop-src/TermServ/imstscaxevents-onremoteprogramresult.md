---
title: Имстскаксевентс Онремотепрограмресулт, метод
description: Вызывается, когда программа RemoteApp возвращает результат в клиентский элемент управления.
ms.assetid: 5bc9570f-14fb-4b6f-a7dd-c1bce3ef19e0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онремотепрограмресулт
- Службы удаленных рабочих столов метода Онремотепрограмресулт, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онремотепрограмресулт
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteProgramResult
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 880e4fb3f6453114415f5bcc07a0afb9c176a1bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136322"
---
# <a name="imstscaxeventsonremoteprogramresult-method"></a><span data-ttu-id="98a40-106">Метод Имстскаксевентс:: Онремотепрограмресулт</span><span class="sxs-lookup"><span data-stu-id="98a40-106">IMsTscAxEvents::OnRemoteProgramResult method</span></span>

<span data-ttu-id="98a40-107">Вызывается, когда программа RemoteApp возвращает результат в клиентский элемент управления.</span><span class="sxs-lookup"><span data-stu-id="98a40-107">Called when a RemoteApp program returns a result to the client control.</span></span>

## <a name="syntax"></a><span data-ttu-id="98a40-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98a40-108">Syntax</span></span>


```C++
VOID OnRemoteProgramResult(
  [in] BSTR                bstrRemoteProgram,
  [in] RemoteProgramResult lError,
  [in] VARIANT_BOOL        vbIsExecutable
);
```



## <a name="parameters"></a><span data-ttu-id="98a40-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="98a40-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98a40-110">*бстрремотепрограм* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="98a40-110">*bstrRemoteProgram* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98a40-111">Имя программы RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="98a40-111">The name of the RemoteApp program.</span></span>

</dd> <dt>

<span data-ttu-id="98a40-112">*леррор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="98a40-112">*lError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98a40-113">Результат попытки запуска программы RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="98a40-113">The result of the attempt to launch the RemoteApp program.</span></span>

<dt>

<span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>

<span data-ttu-id="98a40-114"><span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>**ремотеаппресулток** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="98a40-114"><span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>**remoteAppResultOk** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="98a40-115">Программа RemoteApp успешно запущена.</span><span class="sxs-lookup"><span data-stu-id="98a40-115">The RemoteApp program launched successfully.</span></span>

</dd> <dt>

<span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>

<span data-ttu-id="98a40-116"><span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>**ремотеаппресултлоккед** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="98a40-116"><span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>**remoteAppResultLocked** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="98a40-117">Удаленный сеанс заблокирован, и программа RemoteApp не может быть запущена.</span><span class="sxs-lookup"><span data-stu-id="98a40-117">The remote session is locked and the RemoteApp program cannot be launched.</span></span> <span data-ttu-id="98a40-118">Пользователь должен ввести свои учетные данные, чтобы разблокировать сеанс, а затем запустить программу RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="98a40-118">The user must enter their credentials to unlock the session, and then launch the RemoteApp program.</span></span>

</dd> <dt>

<span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>

<span data-ttu-id="98a40-119"><span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>**ремотеаппресултпротоколеррор** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="98a40-119"><span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>**remoteAppResultProtocolError** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="98a40-120">Программа RemoteApp вернула ошибку протокола.</span><span class="sxs-lookup"><span data-stu-id="98a40-120">The RemoteApp program returned a protocol error.</span></span>

</dd> <dt>

<span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>

<span data-ttu-id="98a40-121"><span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>**ремотеаппресултнотинвхителист** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="98a40-121"><span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>**remoteAppResultNotInWhitelist** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="98a40-122">Программа RemoteApp не находится в списке утвержденных серверов узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="98a40-122">The RemoteApp program is not in the approved list of the RD Session Host server.</span></span>

</dd> <dt>

<span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>

<span data-ttu-id="98a40-123"><span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>**ремотеаппресултнетворкпасдениед** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="98a40-123"><span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>**remoteAppResultNetworkPathDenied** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="98a40-124">Сетевой путь к удаленному приложению RemoteApp был отклонен.</span><span class="sxs-lookup"><span data-stu-id="98a40-124">The network path to the RemoteApp program was denied.</span></span>

</dd> <dt>

<span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>

<span data-ttu-id="98a40-125"><span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>**ремотеаппресултфиленотфаунд** (5 (0x5))</span><span class="sxs-lookup"><span data-stu-id="98a40-125"><span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>**remoteAppResultFileNotFound** (5 (0x5))</span></span>


</dt> <dd>

<span data-ttu-id="98a40-126">Файл программы RemoteApp не найден.</span><span class="sxs-lookup"><span data-stu-id="98a40-126">The RemoteApp program file was not found.</span></span>

</dd> <dt>

<span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>

<span data-ttu-id="98a40-127"><span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>**ремотеаппресултфаилуре** (6 (0x6))</span><span class="sxs-lookup"><span data-stu-id="98a40-127"><span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>**remoteAppResultFailure** (6 (0x6))</span></span>


</dt> <dd>

<span data-ttu-id="98a40-128">Не удалось запустить программу RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="98a40-128">The RemoteApp program failed to launch.</span></span>

</dd> <dt>

<span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>

<span data-ttu-id="98a40-129"><span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>**ремотеаппресулсукнотлоадед** (7 (0x7))</span><span class="sxs-lookup"><span data-stu-id="98a40-129"><span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>**remoteAppResultHookNotLoaded** (7 (0x7))</span></span>


</dt> <dd>

<span data-ttu-id="98a40-130">Невозможно запустить программу RemoteApp, так как в настоящий момент в сеансе отображается защищенный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="98a40-130">The RemoteApp program cannot be launched because the session is currently displaying the secure desktop.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="98a40-131">*вбисексекутабле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="98a40-131">*vbIsExecutable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98a40-132">Указывает, было ли удаленное приложение RemoteApp запущено напрямую с помощью имени исполняемого файла или косвенно с помощью сопоставления файлов.</span><span class="sxs-lookup"><span data-stu-id="98a40-132">Indicates whether the RemoteApp program was launched directly, by using the executable name or indirectly, by using a file association.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98a40-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="98a40-133">Return value</span></span>

<span data-ttu-id="98a40-134">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="98a40-134">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="98a40-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="98a40-135">Remarks</span></span>

<span data-ttu-id="98a40-136">Реализуйте этот метод в приемнике событий, чтобы получить уведомление о том, что программа RemoteApp вернула результат.</span><span class="sxs-lookup"><span data-stu-id="98a40-136">Implement this method in your event sink to receive notification that a RemoteApp program returned a result.</span></span>

<span data-ttu-id="98a40-137">Этот метод вызывается сразу после того, как элемент управления ActiveX пытается запустить программу RemoteApp, а параметр *леррор* указывает результат попытки.</span><span class="sxs-lookup"><span data-stu-id="98a40-137">This method is called immediately after the ActiveX control attempts to launch the RemoteApp program, and the *lError* parameter indicates the result of the attempt.</span></span>

## <a name="requirements"></a><span data-ttu-id="98a40-138">Требования</span><span class="sxs-lookup"><span data-stu-id="98a40-138">Requirements</span></span>



| <span data-ttu-id="98a40-139">Требование</span><span class="sxs-lookup"><span data-stu-id="98a40-139">Requirement</span></span> | <span data-ttu-id="98a40-140">Значение</span><span class="sxs-lookup"><span data-stu-id="98a40-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98a40-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="98a40-141">Minimum supported client</span></span><br/> | <span data-ttu-id="98a40-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="98a40-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="98a40-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="98a40-143">Minimum supported server</span></span><br/> | <span data-ttu-id="98a40-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98a40-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="98a40-145">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="98a40-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="98a40-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98a40-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="98a40-147">DLL</span><span class="sxs-lookup"><span data-stu-id="98a40-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98a40-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98a40-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="98a40-149">IID</span><span class="sxs-lookup"><span data-stu-id="98a40-149">IID</span></span><br/>                      | <span data-ttu-id="98a40-150">Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="98a40-150">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="98a40-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98a40-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98a40-152">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="98a40-152">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





