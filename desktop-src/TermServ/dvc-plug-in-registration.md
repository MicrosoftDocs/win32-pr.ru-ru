---
title: Регистрация подключаемого модуля DVC
description: Описание синтаксиса для записи подключаемого модуля динамического виртуального канала (DVC) для клиента подключение к удаленному рабочему столу (RDC).
ms.assetid: cda4f8c9-867a-41ac-894a-4296d5912b2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 183c73f5f9dda0321640119b2750776d207973cc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672377"
---
# <a name="dvc-plug-in-registration"></a><span data-ttu-id="9617e-103">Регистрация подключаемого модуля DVC</span><span class="sxs-lookup"><span data-stu-id="9617e-103">DVC plug-in registration</span></span>

<span data-ttu-id="9617e-104">Подключаемый модуль динамического виртуального канала (DVC) регистрируется для использования клиентом подключение к удаленному рабочему столу (RDC) с помощью одного из следующих методов.</span><span class="sxs-lookup"><span data-stu-id="9617e-104">The dynamic virtual channel (DVC) plug-in is registered for use by the Remote Desktop Connection (RDC) client using one of the following methods:</span></span>

-   <span data-ttu-id="9617e-105">Вызов метода [**имстскадванцедсеттингс::p UT \_ плугиндллс**](imstscadvancedsettings-plugindlls.md) элемента управления ACTIVEX протокол удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="9617e-105">Invoking the [**IMsTscAdvancedSettings::put\_PluginDlls**](imstscadvancedsettings-plugindlls.md) method of the Remote Desktop Protocol (RDP) ActiveX control.</span></span> <span data-ttu-id="9617e-106">Несколько записей должны быть разделены запятыми.</span><span class="sxs-lookup"><span data-stu-id="9617e-106">Multiple entries must be comma separated.</span></span>
-   <span data-ttu-id="9617e-107">Запись подключаемого модуля находится в следующем расположении в реестре на компьютере, где запущен клиентский процесс подключение к удаленному рабочему столу (RDC):</span><span class="sxs-lookup"><span data-stu-id="9617e-107">Writing the plug-in entry to the following location in the registry on the computer where the Remote Desktop Connection (RDC) client process is started:</span></span>

    <span data-ttu-id="9617e-108">**HKey \_ Текущее \_ пользовательское** \\ **по** \\  \\  \\ **по умолчанию** клиент сервера терминалов Майкрософт \\ **надстройка** \\ ***уникальное имя подключаемого модуля***</span><span class="sxs-lookup"><span data-stu-id="9617e-108">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**Default**\\**AddIns**\\***unique plug-in name***</span></span>

    > [!Note]  
    > <span data-ttu-id="9617e-109">Необходимо создать подраздел *имени подключаемого модуля Unique* , если он не существует.</span><span class="sxs-lookup"><span data-stu-id="9617e-109">You must create the *unique plug-in name* subkey if it does not exist.</span></span> <span data-ttu-id="9617e-110">Уникальное имя подраздела *имени подключаемого модуля* — это произвольная строка, которая может опознать подключаемый модуль.</span><span class="sxs-lookup"><span data-stu-id="9617e-110">The *unique plug-in name* subkey name is an arbitrary string that can identify the plug-in.</span></span> <span data-ttu-id="9617e-111">Строка может быть любым сочетанием символов.</span><span class="sxs-lookup"><span data-stu-id="9617e-111">The string can be any combination of characters.</span></span>

     

    <span data-ttu-id="9617e-112">В разделе *уникальное имя подключаемого модуля* необходимо добавить запись, которая идентифицирует подключаемый модуль.</span><span class="sxs-lookup"><span data-stu-id="9617e-112">Under *unique plug-in name*, you must add an entry that identifies the plug-in.</span></span>

    <span data-ttu-id="9617e-113">Имя записи = **имя**</span><span class="sxs-lookup"><span data-stu-id="9617e-113">Entry name = **Name**</span></span>

    <span data-ttu-id="9617e-114">Тип данных = **reg \_ SZ** или **reg \_ expand \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="9617e-114">Data type = **REG\_SZ** or **REG\_EXPAND\_SZ**</span></span>

<span data-ttu-id="9617e-115">В обоих случаях значение записи должно соответствовать одному из следующих форматов:</span><span class="sxs-lookup"><span data-stu-id="9617e-115">In both cases, the entry value must conform to one of the following formats:</span></span>

<dl> <dt>

<span data-ttu-id="9617e-116"><span id="Plug-inDLLName__CLSID_"></span><span id="plug-indllname__clsid_"></span><span id="PLUG-INDLLNAME__CLSID_"></span>"*Plug-индллнаме*: {*CLSID*}"</span><span class="sxs-lookup"><span data-stu-id="9617e-116"><span id="Plug-inDLLName__CLSID_"></span><span id="plug-indllname__clsid_"></span><span id="PLUG-INDLLNAME__CLSID_"></span>"*Plug-inDLLName*:{*CLSID*}"</span></span>
</dt> <dd>

<span data-ttu-id="9617e-117">Подключаемый модуль не обязательно регистрируется в реестре Windows как объект модели COM, но библиотека DLL реализуется как внутрипроцессный COM-объект.</span><span class="sxs-lookup"><span data-stu-id="9617e-117">The plug-in is not necessarily registered in the Windows registry as a Component Object Model (COM) object, but the DLL is implemented as an in-process COM object.</span></span> <span data-ttu-id="9617e-118">Клиент RDC загрузит библиотеку DLL, указанную в параметре *Plug-индллнаме* , и получите COM-объект непосредственно с помощью *CLSID*.</span><span class="sxs-lookup"><span data-stu-id="9617e-118">The RDC client will load the DLL specified by *Plug-inDLLName* and retrieve the COM object directly using *CLSID*.</span></span>

</dd> <dt>

<span data-ttu-id="9617e-119"><span id="Plug-inDLLName"></span><span id="plug-indllname"></span><span id="PLUG-INDLLNAME"></span>"*Plug-индллнаме*"</span><span class="sxs-lookup"><span data-stu-id="9617e-119"><span id="Plug-inDLLName"></span><span id="plug-indllname"></span><span id="PLUG-INDLLNAME"></span>"*Plug-inDLLName*"</span></span>
</dt> <dd>

<span data-ttu-id="9617e-120">Библиотека DLL реализует функцию [**виртуалчаннелжетинстанце**](virtualchannelgetinstance.md) и экспортирует ее по имени.</span><span class="sxs-lookup"><span data-stu-id="9617e-120">The DLL implements the [**VirtualChannelGetInstance**](virtualchannelgetinstance.md) function and exports it by name.</span></span> <span data-ttu-id="9617e-121">Клиент RDC будет использовать функцию **виртуалчаннелжетинстанце** для получения указателей на интерфейс [**ивтсплугин**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) для всех подключаемых модулей, реализованных библиотекой DLL.</span><span class="sxs-lookup"><span data-stu-id="9617e-121">The RDC client will use the **VirtualChannelGetInstance** function to obtain [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface pointers for all of the plug-ins implemented by the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="9617e-122"><span id="_CLSID_"></span><span id="_clsid_"></span>"{*CLSID*}"</span><span class="sxs-lookup"><span data-stu-id="9617e-122"><span id="_CLSID_"></span><span id="_clsid_"></span>"{*CLSID*}"</span></span>
</dt> <dd>

<span data-ttu-id="9617e-123">Клиент RDC создает экземпляр подключаемого модуля как обычный COM-объект, используя [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) с *идентификатором CLSID*.</span><span class="sxs-lookup"><span data-stu-id="9617e-123">The RDC client will instantiate the plug-in as a regular COM object using [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) with the *CLSID*.</span></span>

</dd> </dl>

> [!Note]  
> <span data-ttu-id="9617e-124">*Plug-индллнаме* представляет полный путь и имя файла DLL.</span><span class="sxs-lookup"><span data-stu-id="9617e-124">*Plug-inDLLName* represents the full path and file name of the .dll file.</span></span> <span data-ttu-id="9617e-125">Если тип данных — **\_ \_ SZ**, путь может содержать неразвернутые переменные среды, которые расширяются во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="9617e-125">If the data type is **REG\_EXPAND\_SZ**, the path can contain unexpanded environment variables that are expanded at runtime.</span></span>

 

<span data-ttu-id="9617e-126">Когда клиент подключение к удаленному рабочему столу (RDC) завершает свою инициализацию, он выполняет следующие действия для каждого зарегистрированного подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="9617e-126">When the Remote Desktop Connection (RDC) client finishes its initialization, it will perform the following for every registered plug-in:</span></span>

1.  <span data-ttu-id="9617e-127">Получите экземпляр интерфейса [**ивтсплугин**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) для каждого подключаемого модуля, используя один из методов, описанных выше.</span><span class="sxs-lookup"><span data-stu-id="9617e-127">Obtain an instance of the [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface for each plug-in using one of the methods described above.</span></span>
2.  <span data-ttu-id="9617e-128">Вызовите метод [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) каждого интерфейса [**ивтсплугин**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) .</span><span class="sxs-lookup"><span data-stu-id="9617e-128">Call the [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) method of each [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface.</span></span>
3.  <span data-ttu-id="9617e-129">Если клиент подключается несколько раз к одному и тому же или к другому серверу, может существовать несколько вызовов [**подключенных**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-connected) и [**отключенных**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-disconnected) методов.</span><span class="sxs-lookup"><span data-stu-id="9617e-129">If the client connects multiple times to the same or to a different server, there may be multiple calls to the [**Connected**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-connected) and [**Disconnected**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-disconnected) methods.</span></span>
4.  <span data-ttu-id="9617e-130">Последний вызов, который должен быть связан с подключаемым модулем, [**завершается**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-terminated).</span><span class="sxs-lookup"><span data-stu-id="9617e-130">The last call that the plug-in should handle is [**Terminated**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-terminated).</span></span> <span data-ttu-id="9617e-131">Это сигнал о том, что клиент подключение к удаленному рабочему столу (RDC) собирается выгрузить подключаемый модуль.</span><span class="sxs-lookup"><span data-stu-id="9617e-131">It is a signal that the Remote Desktop Connection (RDC) client is about to unload the plug-in.</span></span>

 

 