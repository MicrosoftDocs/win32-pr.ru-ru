---
description: API Direct3D 9 работает в модели Windows XP дисплей (XPDM) или Windows Vista дисплей Driver (WDDM) в зависимости от установленной операционной системы.
ms.assetid: b552c822-aa01-4f1d-a0a6-1411ab006e7b
title: XPDM и WDDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12c7d811850c953eb53c346b628363a2642dda9
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343539"
---
# <a name="xpdm-vs-wddm"></a><span data-ttu-id="0502c-103">XPDM и WDDM</span><span class="sxs-lookup"><span data-stu-id="0502c-103">XPDM vs. WDDM</span></span>

<span data-ttu-id="0502c-104">API Direct3D 9 работает в модели Windows XP дисплей (XPDM) или Windows Vista дисплей Driver (WDDM) в зависимости от установленной операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0502c-104">The Direct3D 9 API operates on either the Windows XP display driver model (XPDM) or the Windows Vista display driver model (WDDM), depending on the operating system installed.</span></span> <span data-ttu-id="0502c-105">Существует ряд различий в способе, которым API Direct3D ведет себя в двух моделях драйверов.</span><span class="sxs-lookup"><span data-stu-id="0502c-105">There are some differences in the way the Direct3D API behaves on the two driver models.</span></span>

-   [<span data-ttu-id="0502c-106">Безопасный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="0502c-106">Secure Desktop</span></span>](#secure-desktop)
-   [<span data-ttu-id="0502c-107">Удаленный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="0502c-107">Remote Desktop</span></span>](#remote-desktop)
-   [<span data-ttu-id="0502c-108">Служба Windows</span><span class="sxs-lookup"><span data-stu-id="0502c-108">Windows Service</span></span>](#windows-service)
-   [<span data-ttu-id="0502c-109">См. также</span><span class="sxs-lookup"><span data-stu-id="0502c-109">Related topics</span></span>](#related-topics)

## <a name="secure-desktop"></a><span data-ttu-id="0502c-110">Безопасный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="0502c-110">Secure Desktop</span></span>

<span data-ttu-id="0502c-111">Безопасный рабочий стол активизируется каждый раз, когда происходит любое из следующих условий: пользователь блокирует свой рабочий стол (Windows + L), активируется экранная заставка (если пользователь не вошел в систему) или по умолчанию, когда контроль учетных записей предоставляет запрос.</span><span class="sxs-lookup"><span data-stu-id="0502c-111">The secure desktop is active whenever any of the following occur: the user locks their desktop (Windows+L), the screen saver activates (when no user is logged in), or by default when User Account Control presents a prompt.</span></span> <span data-ttu-id="0502c-112">Когда безопасный рабочий стол активен, устройство HAL недоступно.</span><span class="sxs-lookup"><span data-stu-id="0502c-112">When the secure desktop is active, the HAL device is not accessible.</span></span>

<span data-ttu-id="0502c-113">Различия между XPDM и WDDM:</span><span class="sxs-lookup"><span data-stu-id="0502c-113">Differences between XPDM and WDDM:</span></span>

- <span data-ttu-id="0502c-114">Попытка создать устройство уровня HAL с помощью Direct3D9 завершится сбоем (с **D3DERR \_ \_ недоступно**), а любое существующее устройство Direct3D 9 будет указывать на наличие потерянного кода возврата устройства.</span><span class="sxs-lookup"><span data-stu-id="0502c-114">Attempting to create a Direct3D9 HAL device will fail (with **D3DERR\_NOT\_AVAILABLE**), and any existing Direct3D 9 device will indicate a lost device return code on Present.</span></span>

- <span data-ttu-id="0502c-115">API-интерфейсы Direct3D9Ex и Direct3D 10 могут успешно создавать устройства, пока активен безопасный рабочий стол, и любые вызовы ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) или DXGI) будут возвращать код состояния, указывающий на то, что рабочий стол в данный момент недоступен.</span><span class="sxs-lookup"><span data-stu-id="0502c-115">Direct3D9Ex and Direct3D 10 APIs can successfully create a device while the secure desktop is active, and any calls to Present ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) or DXGI) will return a status code indicating the desktop is currently unavailable.</span></span>



 

## <a name="remote-desktop"></a><span data-ttu-id="0502c-116">Удаленный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="0502c-116">Remote Desktop</span></span>

<span data-ttu-id="0502c-117">Когда удаленный рабочий стол активен, монитор обрабатывается компьютером, на котором размещается компьютер, на котором выполняется отправка сведений через сеть.</span><span class="sxs-lookup"><span data-stu-id="0502c-117">When a remote desktop is active, the display is handled by the viewing machine with the hosting machine sending information via the network.</span></span>

<span data-ttu-id="0502c-118">Различия между XPDM и WDDM:</span><span class="sxs-lookup"><span data-stu-id="0502c-118">Differences between XPDM and WDDM:</span></span>

- <span data-ttu-id="0502c-119">В XPDM все попытки создать устройство Direct3D 9 на удаленном рабочем столе завершатся сбоем.</span><span class="sxs-lookup"><span data-stu-id="0502c-119">On XPDM, all attempts to create a Direct3D 9 device on a remote desktop will fail.</span></span>

- <span data-ttu-id="0502c-120">В WDDM удаленный рабочий стол поддерживает создание устройства HAL через сеанс удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="0502c-120">On WDDM, remote desktop does support creating a HAL device over a remote desktop session.</span></span>



 

## <a name="windows-service"></a><span data-ttu-id="0502c-121">Служба Windows</span><span class="sxs-lookup"><span data-stu-id="0502c-121">Windows Service</span></span>

<span data-ttu-id="0502c-122">Служба Windows — это процесс, выполняемый в фоновом режиме и управляемый диспетчером управления службами (SCM).</span><span class="sxs-lookup"><span data-stu-id="0502c-122">A Windows service is a process that runs in the background, controlled by the service-control manager (SCM).</span></span> <span data-ttu-id="0502c-123">Служба работает независимо от Active Desktop и, следовательно, имеет ограниченную возможность взаимодействовать с пользователями.</span><span class="sxs-lookup"><span data-stu-id="0502c-123">A service runs independent of the active desktop and therefore has limited ability to interact with users.</span></span>

<span data-ttu-id="0502c-124">Различия между XPDM и WDDM:</span><span class="sxs-lookup"><span data-stu-id="0502c-124">Differences between XPDM and WDDM:</span></span>

- <span data-ttu-id="0502c-125">В режиме WDDM изоляция "сеанс 0" гарантирует, что служба не имеет доступа к рабочему столу пользователя в качестве меры безопасности, поэтому устройство Direct3D 9 HAL никогда не будет доступно из службы Windows.</span><span class="sxs-lookup"><span data-stu-id="0502c-125">On WDDM, Session 0 Isolation ensures that a service does not have access to any user desktop as a security measure, therefore, a Direct3D 9 HAL device is never available from a Windows service.</span></span>



 

> [!Note]  
> <span data-ttu-id="0502c-126">Direct3D 9 нельзя использовать в службе Windows.</span><span class="sxs-lookup"><span data-stu-id="0502c-126">You cannot use Direct3D 9 in a Windows service.</span></span> <span data-ttu-id="0502c-127">Дополнительные сведения см. в [статье 978635 технической поддержки Майкрософт](https://support.microsoft.com/kb/978635).</span><span class="sxs-lookup"><span data-stu-id="0502c-127">For more information, see [Microsoft support article 978635](https://support.microsoft.com/kb/978635).</span></span>

 


<span data-ttu-id="0502c-128">В следующей таблице перечислены различия, перечисленные здесь.</span><span class="sxs-lookup"><span data-stu-id="0502c-128">The following table summarizes the differences listed here.</span></span>



| <span data-ttu-id="0502c-129">Безопасный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="0502c-129">Secure Desktop</span></span> | <span data-ttu-id="0502c-130">ДРАЙВЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0502c-130">XPDM</span></span> | <span data-ttu-id="0502c-131">WDDM (Direct3D9)</span><span class="sxs-lookup"><span data-stu-id="0502c-131">WDDM (Direct3D9)</span></span> | <span data-ttu-id="0502c-132">WDDM (Direct3D9Ex/Direct3D10)</span><span class="sxs-lookup"><span data-stu-id="0502c-132">WDDM(Direct3D9Ex/Direct3D10)</span></span> |
|-----------------|------|------------------|------------------------------|
| <span data-ttu-id="0502c-133">нуллреф</span><span class="sxs-lookup"><span data-stu-id="0502c-133">NULLREF</span></span>         | <span data-ttu-id="0502c-134">Да</span><span class="sxs-lookup"><span data-stu-id="0502c-134">Yes</span></span>  | <span data-ttu-id="0502c-135">Да</span><span class="sxs-lookup"><span data-stu-id="0502c-135">Yes</span></span>              | <span data-ttu-id="0502c-136">Да</span><span class="sxs-lookup"><span data-stu-id="0502c-136">Yes</span></span>                          |
| <span data-ttu-id="0502c-137">ПРОЦЕССОР</span><span class="sxs-lookup"><span data-stu-id="0502c-137">HAL</span></span>             | <span data-ttu-id="0502c-138">Нет</span><span class="sxs-lookup"><span data-stu-id="0502c-138">No</span></span>   | <span data-ttu-id="0502c-139">Нет</span><span class="sxs-lookup"><span data-stu-id="0502c-139">No</span></span>               | <span data-ttu-id="0502c-140">Да</span><span class="sxs-lookup"><span data-stu-id="0502c-140">Yes</span></span>                          |
| <span data-ttu-id="0502c-141">REF</span><span class="sxs-lookup"><span data-stu-id="0502c-141">REF</span></span>             | <span data-ttu-id="0502c-142">Да</span><span class="sxs-lookup"><span data-stu-id="0502c-142">Yes</span></span>  | <span data-ttu-id="0502c-143">Да</span><span class="sxs-lookup"><span data-stu-id="0502c-143">Yes</span></span>              | <span data-ttu-id="0502c-144">Да</span><span class="sxs-lookup"><span data-stu-id="0502c-144">Yes</span></span>                          |
| <span data-ttu-id="0502c-145">Удаленный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="0502c-145">Remote Desktop</span></span>  |      |                  |                              |
| <span data-ttu-id="0502c-146">нуллреф</span><span class="sxs-lookup"><span data-stu-id="0502c-146">NULLREF</span></span>         | <span data-ttu-id="0502c-147">Нет</span><span class="sxs-lookup"><span data-stu-id="0502c-147">No</span></span>   | <span data-ttu-id="0502c-148">Да</span><span class="sxs-lookup"><span data-stu-id="0502c-148">Yes</span></span>              | <span data-ttu-id="0502c-149">Да</span><span class="sxs-lookup"><span data-stu-id="0502c-149">Yes</span></span>                          |
| <span data-ttu-id="0502c-150">ПРОЦЕССОР</span><span class="sxs-lookup"><span data-stu-id="0502c-150">HAL</span></span>             | <span data-ttu-id="0502c-151">Нет</span><span class="sxs-lookup"><span data-stu-id="0502c-151">No</span></span>   | <span data-ttu-id="0502c-152">Да</span><span class="sxs-lookup"><span data-stu-id="0502c-152">Yes</span></span>              | <span data-ttu-id="0502c-153">Да</span><span class="sxs-lookup"><span data-stu-id="0502c-153">Yes</span></span>                          |
| <span data-ttu-id="0502c-154">REF</span><span class="sxs-lookup"><span data-stu-id="0502c-154">REF</span></span>             | <span data-ttu-id="0502c-155">Да</span><span class="sxs-lookup"><span data-stu-id="0502c-155">Yes</span></span>  | <span data-ttu-id="0502c-156">Да</span><span class="sxs-lookup"><span data-stu-id="0502c-156">Yes</span></span>              | <span data-ttu-id="0502c-157">Да</span><span class="sxs-lookup"><span data-stu-id="0502c-157">Yes</span></span>                          |
| <span data-ttu-id="0502c-158">Служба Windows</span><span class="sxs-lookup"><span data-stu-id="0502c-158">Windows Service</span></span> |      |                  |                              |
| <span data-ttu-id="0502c-159">нуллреф</span><span class="sxs-lookup"><span data-stu-id="0502c-159">NULLREF</span></span>         | <span data-ttu-id="0502c-160">Нет</span><span class="sxs-lookup"><span data-stu-id="0502c-160">No</span></span>   | <span data-ttu-id="0502c-161">Нет</span><span class="sxs-lookup"><span data-stu-id="0502c-161">No</span></span>               | <span data-ttu-id="0502c-162">Нет</span><span class="sxs-lookup"><span data-stu-id="0502c-162">No</span></span>                           |
| <span data-ttu-id="0502c-163">ПРОЦЕССОР</span><span class="sxs-lookup"><span data-stu-id="0502c-163">HAL</span></span>             | <span data-ttu-id="0502c-164">Нет</span><span class="sxs-lookup"><span data-stu-id="0502c-164">No</span></span>   | <span data-ttu-id="0502c-165">Нет</span><span class="sxs-lookup"><span data-stu-id="0502c-165">No</span></span>               | <span data-ttu-id="0502c-166">Нет</span><span class="sxs-lookup"><span data-stu-id="0502c-166">No</span></span>                           |
| <span data-ttu-id="0502c-167">REF</span><span class="sxs-lookup"><span data-stu-id="0502c-167">REF</span></span>             | <span data-ttu-id="0502c-168">Нет</span><span class="sxs-lookup"><span data-stu-id="0502c-168">No</span></span>   | <span data-ttu-id="0502c-169">Нет</span><span class="sxs-lookup"><span data-stu-id="0502c-169">No</span></span>               | <span data-ttu-id="0502c-170">Нет</span><span class="sxs-lookup"><span data-stu-id="0502c-170">No</span></span>                           |
| <span data-ttu-id="0502c-171">WARP10</span><span class="sxs-lookup"><span data-stu-id="0502c-171">WARP10</span></span>          | <span data-ttu-id="0502c-172">Н/Д</span><span class="sxs-lookup"><span data-stu-id="0502c-172">N/A</span></span>  | <span data-ttu-id="0502c-173">Н/Д</span><span class="sxs-lookup"><span data-stu-id="0502c-173">N/A</span></span>              | <span data-ttu-id="0502c-174">Да</span><span class="sxs-lookup"><span data-stu-id="0502c-174">Yes</span></span>                          |



 

<span data-ttu-id="0502c-175">Дополнительные сведения о модели XPDM, WDDM, Direct3D9Ex и Direct3D 10 см. [в статье интерфейсы API графики в Windows](../direct3darticles/graphics-apis-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="0502c-175">For more information about XPDM, WDDM, Direct3D9Ex, and Direct3D 10, see [Graphics APIs in Windows](../direct3darticles/graphics-apis-in-windows-vista.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0502c-176">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="0502c-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0502c-177">Устройства Direct3D</span><span class="sxs-lookup"><span data-stu-id="0502c-177">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
