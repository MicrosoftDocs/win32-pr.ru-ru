---
description: Можно выбрать компьютер в службе Центр обновления Майкрософт, а затем зарегистрировать эту службу в автоматическое обновление.
ms.assetid: d6f3d8ca-3b7e-409c-87b6-db247b7b68e4
title: Opt-In Центр обновления Майкрософт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b149eb28024d77f66a08371827187adf05d4b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143684"
---
# <a name="opt-in-to-microsoft-update"></a><span data-ttu-id="55125-103">Opt-In Центр обновления Майкрософт</span><span class="sxs-lookup"><span data-stu-id="55125-103">Opt-In to Microsoft Update</span></span>

<span data-ttu-id="55125-104">Можно выбрать компьютер в службе Центр обновления Майкрософт, а затем зарегистрировать эту службу в автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="55125-104">You can opt a computer in to the Microsoft Update service and then register that service with Automatic Updates.</span></span>

<span data-ttu-id="55125-105">В примере сценариев в этом разделе показано, как использовать агент Центр обновления Windows (WUA) для регистрации службы Центр обновления Майкрософт с автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="55125-105">The scripting sample in this topic shows you how to use Windows Update Agent (WUA) to register the Microsoft Update service with Automatic Updates.</span></span> <span data-ttu-id="55125-106">Кроме того, чтобы зарегистрировать службу, пользователь может посетить Центр обновления Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="55125-106">Alternatively, to register the service, the user can visit Microsoft Update.</span></span>

<span data-ttu-id="55125-107">Перед запуском этого образца убедитесь, что на компьютере установлена версия WUA 7.0.6000 или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="55125-107">Before you attempt to run this sample, verify that the version of WUA that is installed on the computer is version 7.0.6000 or a later version.</span></span> <span data-ttu-id="55125-108">Дополнительные сведения о том, как определить версию установленного агента WUA, см. [в разделе Определение текущей версии WUA](determining-the-current-version-of-wua.md).</span><span class="sxs-lookup"><span data-stu-id="55125-108">For more information about how to determine the version of WUA that is installed, see [Determining the Current Version of WUA](determining-the-current-version-of-wua.md).</span></span>

## <a name="example"></a><span data-ttu-id="55125-109">Пример</span><span class="sxs-lookup"><span data-stu-id="55125-109">Example</span></span>

<span data-ttu-id="55125-110">В следующем примере сценария показано, как с помощью агента Центр обновления Windows (WUA) зарегистрировать службу Центр обновления Майкрософт с автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="55125-110">The following scripting sample shows you how to use the Windows Update Agent (WUA) to register the Microsoft Update service with Automatic Updates.</span></span> <span data-ttu-id="55125-111">Пример разрешает отложенную или автономную обработку при необходимости.</span><span class="sxs-lookup"><span data-stu-id="55125-111">The sample allows deferred or offline processing if needed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="55125-112">Этот сценарий предназначен для демонстрации использования API-интерфейсов агента Центр обновления Windows и предоставления примера того, как разработчики могут использовать эти API для решения проблем.</span><span class="sxs-lookup"><span data-stu-id="55125-112">This script is intended to demonstrate the use of the Windows Update Agent APIs, and provide an example of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="55125-113">Этот сценарий не предназначен для рабочего кода, и сам сценарий не поддерживается корпорацией Майкрософт (хотя поддерживаются базовые API-интерфейсы Центр обновления Windows агента).</span><span class="sxs-lookup"><span data-stu-id="55125-113">This script is not intended as production code, and the script itself is not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 


```VB
Set ServiceManager = CreateObject("Microsoft.Update.ServiceManager")
ServiceManager.ClientApplicationID = "My App"

'add the Microsoft Update Service, GUID
Set NewUpdateService = ServiceManager.AddService2("7971f918-a847-4430-9279-4a52d1efe18d",7,"")

```



<span data-ttu-id="55125-114">В более ранних версиях WUA (минимальная версия 7.0.6000) можно упростить процесс согласия с помощью параметра реестра.</span><span class="sxs-lookup"><span data-stu-id="55125-114">In earlier versions of WUA (a minimum WUA version of 7.0.6000), you can simplify the opt-in process by using a registry setting.</span></span> <span data-ttu-id="55125-115">После того как раздел и значения реестра настроены, процесс согласия Центр обновления Майкрософт выполняется в следующий раз, когда WUA выполняет поиск.</span><span class="sxs-lookup"><span data-stu-id="55125-115">After the registry key and values are configured, the Microsoft Update opt-in process occurs the next time WUA performs a search.</span></span> <span data-ttu-id="55125-116">Процесс согласия может инициироваться автоматическое обновление или вызывающим объектом API.</span><span class="sxs-lookup"><span data-stu-id="55125-116">The opt-in process may be triggered by Automatic Updates or by an API caller.</span></span>

<span data-ttu-id="55125-117">Например, полный путь к разделу реестра и значения, которые необходимо задать для процесса включения, выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="55125-117">For example, the full path of the registry key and values to set for the opt-in process are as follows:</span></span>

<span data-ttu-id="55125-118">**HKLM** \\ **Программное обеспечение** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Windowsupdate** \\ **Пендингсервицерегистратион** \\ **7971f918-A847-4430-9279-4a52d1efe18d**</span><span class="sxs-lookup"><span data-stu-id="55125-118">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**WindowsUpdate**\\**PendingServiceRegistration**\\**7971f918-a847-4430-9279-4a52d1efe18d**</span></span>

<span data-ttu-id="55125-119">**Клиентаппликатионид** = мое приложение</span><span class="sxs-lookup"><span data-stu-id="55125-119">**ClientApplicationID** = My App</span></span>

<span data-ttu-id="55125-120">**Регистервисау** = 1</span><span class="sxs-lookup"><span data-stu-id="55125-120">**RegisterWithAU** = 1</span></span>

> [!Note]
>
> <span data-ttu-id="55125-121">Раздел реестра учитывается только при обновлении агента WUA с версии, предшествующей версии 7.0.6000, до версии 7.0.6000 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="55125-121">The registry key is respected once only when WUA is updated from a version that is earlier than version 7.0.6000 to version 7.0.6000 or to a later version.</span></span> <span data-ttu-id="55125-122">Мы рекомендуем применять при перезаписи существующих значений реестра, поскольку перезапись значений может привести к изменению результатов предыдущего запроса на регистрацию службы.</span><span class="sxs-lookup"><span data-stu-id="55125-122">We recommend discretion when overwriting existing registry values because overwriting the values may change the result of an earlier service registration request.</span></span>
>
> <span data-ttu-id="55125-123">Для создания этого раздела реестра требуются учетные данные администратора.</span><span class="sxs-lookup"><span data-stu-id="55125-123">Creating this registry key requires administrative credentials.</span></span> <span data-ttu-id="55125-124">В Windows Vista вызывающий объект должен создать раздел реестра в процессе с повышенными правами.</span><span class="sxs-lookup"><span data-stu-id="55125-124">For Windows Vista, the caller must create the registry key in an elevated process.</span></span>

 

 

 



