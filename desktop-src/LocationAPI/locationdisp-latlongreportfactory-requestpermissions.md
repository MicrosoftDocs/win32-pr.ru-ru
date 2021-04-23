---
description: Открывает диалоговое окно системы, в котором запрашиваются разрешения пользователя для устройств с поддержкой расположения.
ms.assetid: 25b4368d-ff9d-4806-a22e-4ae0760d6f0f
title: Локатиондисп. Латлонгрепортфактори. Рекуестпермиссионс, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.RequestPermissions
api_type:
- COM
api_location: ''
ms.openlocfilehash: ed789aca4b6c9d0db50a3e7b6cae33d55d22920c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673941"
---
# <a name="locationdisplatlongreportfactoryrequestpermissions-method"></a><span data-ttu-id="c1025-103">Локатиондисп. Латлонгрепортфактори. Рекуестпермиссионс, метод</span><span class="sxs-lookup"><span data-stu-id="c1025-103">LocationDisp.LatLongReportFactory.RequestPermissions method</span></span>

<span data-ttu-id="c1025-104">\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="c1025-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c1025-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="c1025-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="c1025-106">Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c1025-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="c1025-107">Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="c1025-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="c1025-108">Открывает диалоговое окно системы, в котором запрашиваются разрешения пользователя для устройств с поддержкой расположения.</span><span class="sxs-lookup"><span data-stu-id="c1025-108">Opens a system dialog box to request user permission for location-enabled devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1025-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1025-109">Syntax</span></span>


```JScript
LocationDisp.LatLongReportFactory.RequestPermissions(
  hWnd
)
```



## <a name="parameters"></a><span data-ttu-id="c1025-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1025-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1025-111">*hWnd*</span><span class="sxs-lookup"><span data-stu-id="c1025-111">*hWnd*</span></span> 
</dt> <dd>

<span data-ttu-id="c1025-112">Этот параметр не используется и должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="c1025-112">This parameter is not used and should be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1025-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1025-113">Return value</span></span>

<span data-ttu-id="c1025-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c1025-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1025-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1025-115">Remarks</span></span>

<span data-ttu-id="c1025-116">Вызов является синхронным, и вызывающий объект ожидает закрытия диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="c1025-116">The call is synchronous and the caller waits for the dialog box to be closed.</span></span>

> [!Note]  
> <span data-ttu-id="c1025-117">Если приложение, работающее в защищенном режиме, например объект модуля поддержки браузера (BHO) для Internet Explorer, вызывает **рекуестпермиссионс**, и пользователь выбирает параметр **не включать этот датчик расположения** в диалоговом окне, поставщик расположения не будет включен, но Windows снова отобразит это диалоговое окно, если **рекуестпермиссионс** повторно вызывается этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="c1025-117">If an application running in protected mode, such as a Browser Helper Object (BHO) for Internet Explorer, calls **RequestPermissions**, and the user chooses the **Don't enable this location sensor** option in the dialog box, the location provider will not be enabled, but Windows will display the dialog box again if **RequestPermissions** is called again by the same user.</span></span> <span data-ttu-id="c1025-118">Приложения, работающие в защищенном режиме, могут не вызывать **рекуестпермиссионс** при запуске, чтобы пользователь не мог видеть потенциально нежелательное диалоговое окно при каждом запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="c1025-118">Applications that run in protected mode may choose to not call **RequestPermissions** on startup so that the user does not see a possibly unwanted dialog box each time the application starts.</span></span>

 

## <a name="examples"></a><span data-ttu-id="c1025-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="c1025-119">Examples</span></span>

<span data-ttu-id="c1025-120">Пример использования этого метода см. в разделе [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="c1025-120">For an example of how to use this method, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1025-121">Требования</span><span class="sxs-lookup"><span data-stu-id="c1025-121">Requirements</span></span>



| <span data-ttu-id="c1025-122">Требование</span><span class="sxs-lookup"><span data-stu-id="c1025-122">Requirement</span></span> | <span data-ttu-id="c1025-123">Значение</span><span class="sxs-lookup"><span data-stu-id="c1025-123">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="c1025-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c1025-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c1025-125">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c1025-125">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c1025-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c1025-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c1025-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c1025-127">None supported</span></span><br/>                  |



 

