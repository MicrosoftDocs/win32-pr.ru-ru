---
title: Имстскаксевентс Онрекуестгофуллскрин, метод
description: Вызывается, когда клиент запрашивает переключение в полноэкранный режим и \_ вызывается метод имстскадванцедсеттингс Set контаинерхандледфуллскрин, чтобы установить свойство контаинерхандледфуллскрин в ненулевое значение.
ms.assetid: f61520dc-a72a-4205-8761-92aaf08b5f90
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онрекуестгофуллскрин
- Службы удаленных рабочих столов метода Онрекуестгофуллскрин, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онрекуестгофуллскрин
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestGoFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c865cd27b447743f781b8563956e7fb2d7f5d703
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415752"
---
# <a name="imstscaxeventsonrequestgofullscreen-method"></a><span data-ttu-id="d547c-106">Метод Имстскаксевентс:: Онрекуестгофуллскрин</span><span class="sxs-lookup"><span data-stu-id="d547c-106">IMsTscAxEvents::OnRequestGoFullScreen method</span></span>

<span data-ttu-id="d547c-107">Вызывается, когда клиент запрашивает переключение в полноэкранный режим и вызывается метод [**имстскадванцедсеттингс::p UT \_ контаинерхандледфуллскрин**](imstscadvancedsettings-containerhandledfullscreen.md) , чтобы установить свойство **контаинерхандледфуллскрин** в ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="d547c-107">Called when the client requests to switch to full-screen mode and the [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) method is called to set the **ContainerHandledFullScreen** property to a nonzero value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d547c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d547c-108">Syntax</span></span>


```C++
void OnRequestGoFullScreen();
```



## <a name="parameters"></a><span data-ttu-id="d547c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d547c-109">Parameters</span></span>

<span data-ttu-id="d547c-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d547c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d547c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d547c-111">Return value</span></span>

<span data-ttu-id="d547c-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d547c-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d547c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d547c-113">Remarks</span></span>

<span data-ttu-id="d547c-114">В полноэкранном режиме, поддерживающем контейнеры, контейнер должен войти в стандартный полноэкранный режим в ответ на это событие.</span><span class="sxs-lookup"><span data-stu-id="d547c-114">In container-handled full-screen mode, the container should enter standard full-screen mode in response to this event.</span></span>

<span data-ttu-id="d547c-115">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d547c-115">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d547c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d547c-116">Requirements</span></span>



| <span data-ttu-id="d547c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="d547c-117">Requirement</span></span> | <span data-ttu-id="d547c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d547c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d547c-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d547c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d547c-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d547c-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d547c-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d547c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d547c-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d547c-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d547c-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d547c-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="d547c-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d547c-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d547c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d547c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d547c-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d547c-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d547c-127">IID</span><span class="sxs-lookup"><span data-stu-id="d547c-127">IID</span></span><br/>                      | <span data-ttu-id="d547c-128">Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="d547c-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="d547c-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d547c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d547c-130">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="d547c-130">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





