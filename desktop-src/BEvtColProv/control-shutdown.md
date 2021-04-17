---
description: Останавливает сборщик. Если сборщик работает в качестве службы, то остановка службы является лучшим подходом.
ms.assetid: fab3e060-156f-46f5-98a2-d47a23d64552
ms.tgt_platform: multiple
title: Метод Shutdown класса Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Shutdown
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: d401ac528498d7b8ab5ccacbf6a0b5bf781555f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655652"
---
# <a name="shutdown-method-of-the-control-class"></a><span data-ttu-id="838bd-104">Метод Shutdown класса Control</span><span class="sxs-lookup"><span data-stu-id="838bd-104">Shutdown method of the Control class</span></span>

<span data-ttu-id="838bd-105">Останавливает сборщик.</span><span class="sxs-lookup"><span data-stu-id="838bd-105">Stops the collector.</span></span> <span data-ttu-id="838bd-106">Если сборщик работает в качестве службы, то остановка службы является лучшим подходом.</span><span class="sxs-lookup"><span data-stu-id="838bd-106">If the collector is running as a service, stopping the service is the better approach.</span></span>

## <a name="syntax"></a><span data-ttu-id="838bd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="838bd-107">Syntax</span></span>


```mof
void Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="838bd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="838bd-108">Parameters</span></span>

<span data-ttu-id="838bd-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="838bd-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="838bd-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="838bd-110">Return value</span></span>

<span data-ttu-id="838bd-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="838bd-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="838bd-112">Требования</span><span class="sxs-lookup"><span data-stu-id="838bd-112">Requirements</span></span>



| <span data-ttu-id="838bd-113">Требование</span><span class="sxs-lookup"><span data-stu-id="838bd-113">Requirement</span></span> | <span data-ttu-id="838bd-114">Значение</span><span class="sxs-lookup"><span data-stu-id="838bd-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="838bd-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="838bd-115">Minimum supported client</span></span><br/> | <span data-ttu-id="838bd-116">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="838bd-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="838bd-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="838bd-117">Minimum supported server</span></span><br/> | <span data-ttu-id="838bd-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="838bd-118">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="838bd-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="838bd-119">Namespace</span></span><br/>                | <span data-ttu-id="838bd-120">Корневой \\ узел Microsoft \\ Windows \\ бутевентколлектор</span><span class="sxs-lookup"><span data-stu-id="838bd-120">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="838bd-121">MOF</span><span class="sxs-lookup"><span data-stu-id="838bd-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="838bd-122"><dt>Бутевентколлекторвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="838bd-122"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="838bd-123">DLL</span><span class="sxs-lookup"><span data-stu-id="838bd-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="838bd-124"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="838bd-124"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="838bd-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="838bd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="838bd-126">**Элемента**</span><span class="sxs-lookup"><span data-stu-id="838bd-126">**Control**</span></span>](control.md)
</dt> </dl>

 

 




