---
description: Включает сетевой адаптер.
ms.assetid: ceb71e1b-5107-420f-a677-814307340469
ms.tgt_platform: multiple
title: Enable, метод класса Win32_NetworkAdapter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapter.Enable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7a7653d0bcda28ca333bc5c70bdcd69bce382787
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262594"
---
# <a name="enable-method-of-the-win32_networkadapter-class"></a><span data-ttu-id="649e9-103">Enable, метод класса Win32 \_ сетевого адаптера</span><span class="sxs-lookup"><span data-stu-id="649e9-103">Enable method of the Win32\_NetworkAdapter class</span></span>

<span data-ttu-id="649e9-104">Метод **Enable** включает сетевой адаптер.</span><span class="sxs-lookup"><span data-stu-id="649e9-104">The **Enable** method enables the network adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="649e9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="649e9-105">Syntax</span></span>


```mof
uint32 Enable();
```



## <a name="parameters"></a><span data-ttu-id="649e9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="649e9-106">Parameters</span></span>

<span data-ttu-id="649e9-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="649e9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="649e9-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="649e9-108">Return value</span></span>

<span data-ttu-id="649e9-109">Возвращает ноль (0), чтобы указать на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="649e9-109">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="649e9-110">Любое другое значение указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="649e9-110">Any other number indicates an error.</span></span> <span data-ttu-id="649e9-111">Коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="649e9-111">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="remarks"></a><span data-ttu-id="649e9-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="649e9-112">Remarks</span></span>

<span data-ttu-id="649e9-113">Вы можете столкнуться с трудностями при использовании этого метода, если приложение не имеет прав администратора привилиджес.</span><span class="sxs-lookup"><span data-stu-id="649e9-113">You may experience difficulty using this method if your application does not administrator access privilidges.</span></span>

## <a name="examples"></a><span data-ttu-id="649e9-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="649e9-114">Examples</span></span>

<span data-ttu-id="649e9-115">В следующем примере скрипта Visual Basic включается первый сетевой адаптер и отображается состояние свойства **NetEnabled** .</span><span class="sxs-lookup"><span data-stu-id="649e9-115">The following Visual Basic Script example enables the first network adapter and shows the status of the **NetEnabled** property.</span></span> <span data-ttu-id="649e9-116">Дополнительные сведения см. в разделе [**SWbemObjectSet. итеминдекс**](/windows/desktop/wmisdk/swbemobjectset-itemindex).</span><span class="sxs-lookup"><span data-stu-id="649e9-116">For more information, see [**SWbemObjectSet.ItemIndex**](/windows/desktop/wmisdk/swbemobjectset-itemindex).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colAdapters = _
    objWMIService.Execquery_
        ("Select * from Win32_NetworkAdapter Where NetEnabled=False")
For Each Adapter in colAdapters
    WScript.Echo Adapter.DeviceId & "    " & Adapter.Name
Next
errReturn = colAdapters.ItemIndex(0).Enable()
If errReturn <> 0 Then
    WScript.Echo "Enable Network adapter failed for adapter= "_
        & colAdapters.ItemIndex(0).DeviceId
Else 
    WScript.Echo "Enable Network adapter succeeded for adapter= "_
        & colAdapters.ItemIndex(0).DeviceId 
End If 
WScript.Echo "NetEnabled= " & colAdapters.ItemIndex(0).NetEnabled
```



## <a name="requirements"></a><span data-ttu-id="649e9-117">Требования</span><span class="sxs-lookup"><span data-stu-id="649e9-117">Requirements</span></span>



| <span data-ttu-id="649e9-118">Требование</span><span class="sxs-lookup"><span data-stu-id="649e9-118">Requirement</span></span> | <span data-ttu-id="649e9-119">Значение</span><span class="sxs-lookup"><span data-stu-id="649e9-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="649e9-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="649e9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="649e9-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="649e9-121">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="649e9-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="649e9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="649e9-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="649e9-123">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="649e9-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="649e9-124">Namespace</span></span><br/>                | <span data-ttu-id="649e9-125">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="649e9-125">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="649e9-126">MOF</span><span class="sxs-lookup"><span data-stu-id="649e9-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="649e9-127"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="649e9-127"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="649e9-128">DLL</span><span class="sxs-lookup"><span data-stu-id="649e9-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="649e9-129"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="649e9-129"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="649e9-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="649e9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="649e9-131">**\_Сетевого адаптера Win32**</span><span class="sxs-lookup"><span data-stu-id="649e9-131">**Win32\_NetworkAdapter**</span></span>](win32-networkadapter.md)
</dt> <dt>

[<span data-ttu-id="649e9-132">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="649e9-132">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="649e9-133">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="649e9-133">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

