---
title: Настройка службы имен
description: Начиная с Windows 2000, при установке Windows SDK программа установки автоматически выбирает локатор Майкрософт в качестве поставщика службы имен. Поставщик службы имен можно изменить с помощью панели управления.
ms.assetid: bd72ca2f-bb93-4057-a877-be755a88719d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c1c895aecb3bdf74189461cd6aa9ee814b2d68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486777"
---
# <a name="configuring-the-name-service"></a><span data-ttu-id="78a66-104">Настройка службы имен</span><span class="sxs-lookup"><span data-stu-id="78a66-104">Configuring the Name Service</span></span>

<span data-ttu-id="78a66-105">Начиная с Windows 2000, при установке Windows SDK программа установки автоматически выбирает локатор Майкрософт в качестве поставщика службы имен.</span><span class="sxs-lookup"><span data-stu-id="78a66-105">Starting with Windows 2000, when you install the Windows SDK, the setup program automatically selects Microsoft Locator as the name service provider.</span></span> <span data-ttu-id="78a66-106">Поставщик службы имен можно изменить с помощью панели управления.</span><span class="sxs-lookup"><span data-stu-id="78a66-106">You can change the name service provider through Control Panel.</span></span>

<span data-ttu-id="78a66-107">Главный компьютер, на котором работает нсид, выступает в качестве шлюза для службы каталогов ячеек DCE, передающий вызовы функций NSI между компьютерами, на которых работают операционные системы Майкрософт и компьютеры DCE.</span><span class="sxs-lookup"><span data-stu-id="78a66-107">The host computer that runs the nsid acts as a gateway to the DCE Cell Directory Service, passing NSI function calls between computers that run Microsoft operating systems and DCE computers.</span></span> <span data-ttu-id="78a66-108">Сетевой адрес может содержать до 80 символов, например, 11.1.9.169 является допустимым адресом.</span><span class="sxs-lookup"><span data-stu-id="78a66-108">A network address can be up to 80 characters—for example, 11.1.9.169 is a valid address.</span></span>

> [!Note]  
> <span data-ttu-id="78a66-109">Для настройки компакт-дисков DCE в качестве поставщика службы имен необходимо иметь продукт устройства DCE с цифровым оборудованием.</span><span class="sxs-lookup"><span data-stu-id="78a66-109">You must have the Digital Equipment Corporation DCE CDS product to configure the DCE CDS as your name service provider.</span></span> <span data-ttu-id="78a66-110">Сведения о компакт-дисках DCE см. в документации, предоставляемой корпорацией Digital Equipment.</span><span class="sxs-lookup"><span data-stu-id="78a66-110">See the documentation provided by Digital Equipment Corporation for information about DCE CDS.</span></span>

 

<span data-ttu-id="78a66-111">**Перенастройка поставщика службы имен**</span><span class="sxs-lookup"><span data-stu-id="78a66-111">**To reconfigure the name service provider**</span></span>

1.  <span data-ttu-id="78a66-112">На панели управления щелкните значок " **Сетевые подключения** ".</span><span class="sxs-lookup"><span data-stu-id="78a66-112">In Control Panel, click the **Network Connections** icon.</span></span> <span data-ttu-id="78a66-113">Откроется окно " **Сетевые подключения** ".</span><span class="sxs-lookup"><span data-stu-id="78a66-113">The **Network Connections** window appears.</span></span>
2.  <span data-ttu-id="78a66-114">Выберите сетевое подключение для настройки, щелкните его правой кнопкой мыши и выберите в контекстном меню пункт **Свойства** .</span><span class="sxs-lookup"><span data-stu-id="78a66-114">Select the network connection to configure, right-click, and select **Properties** from the context menu.</span></span> <span data-ttu-id="78a66-115">Откроется диалоговое окно **Свойства соединения** .</span><span class="sxs-lookup"><span data-stu-id="78a66-115">The **Connection Properties** dialog appears.</span></span>
3.  <span data-ttu-id="78a66-116">В диалоговом окне **Свойства соединения** выберите **клиент для сетей Microsoft** и нажмите кнопку **Свойства** .</span><span class="sxs-lookup"><span data-stu-id="78a66-116">In the **Connection Properties** dialog, select **Client for Microsoft Networks** and click the **Properties** button.</span></span> <span data-ttu-id="78a66-117">Откроется диалоговое окно **Свойства клиента для сети Microsoft** .</span><span class="sxs-lookup"><span data-stu-id="78a66-117">The **Client for Microsoft Network Properties** dialog appears.</span></span>
4.  <span data-ttu-id="78a66-118">В диалоговом окне **Свойства клиента для сети Microsoft** откройте раскрывающийся список **поставщик службы имен** и выберите поставщика имен из списка.</span><span class="sxs-lookup"><span data-stu-id="78a66-118">In the **Client for Microsoft Network Properties** dialog, open the **Name service provider** drop-down and select a name provider from the list.</span></span>
    1.  <span data-ttu-id="78a66-119">При выборе указателя Майкрософт нажмите кнопку ОК.</span><span class="sxs-lookup"><span data-stu-id="78a66-119">When you select Microsoft Locator, click OK.</span></span> <span data-ttu-id="78a66-120">После этого процесс настройки завершится.</span><span class="sxs-lookup"><span data-stu-id="78a66-120">The configuration process is then complete.</span></span>
    2.  <span data-ttu-id="78a66-121">При выборе службы каталогов ячеек DCE в поле **сетевой адрес** введите имя главного компьютера, на котором работает управляющая программа NSI (нсид), и нажмите кнопку ОК.</span><span class="sxs-lookup"><span data-stu-id="78a66-121">When you select the DCE Cell Directory Service, in the **Network Address** box, type the name of the host computer that runs the NSI daemon (nsid), and then click OK.</span></span>

<span data-ttu-id="78a66-122">**Перенастройка поставщика службы имен для Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="78a66-122">**To reconfigure the name service provider for Windows 2000**</span></span>

1.  <span data-ttu-id="78a66-123">На панели управления щелкните значок **сети** .</span><span class="sxs-lookup"><span data-stu-id="78a66-123">In Control Panel, click the **Network** icon.</span></span>

    <span data-ttu-id="78a66-124">Откроется диалоговое окно **сеть** .</span><span class="sxs-lookup"><span data-stu-id="78a66-124">The **Network** dialog box appears.</span></span>

2.  <span data-ttu-id="78a66-125">В диалоговом окне **сеть** нажмите кнопку **настроить**.</span><span class="sxs-lookup"><span data-stu-id="78a66-125">In the **Network** dialog box, click **Configure**.</span></span>
3.  <span data-ttu-id="78a66-126">В списке **нетворксофтваре** выберите **Конфигурация RPC**.</span><span class="sxs-lookup"><span data-stu-id="78a66-126">In the **NetworkSoftware** list, select **RPC Configuration**.</span></span>

    <span data-ttu-id="78a66-127">Откроется диалоговое окно **Конфигурация поставщика службы имен RPC** .</span><span class="sxs-lookup"><span data-stu-id="78a66-127">The **RPC Name Service Provider Configuration** dialog box appears.</span></span>

4.  <span data-ttu-id="78a66-128">В диалоговом окне **Конфигурация поставщика службы имен RPC** выберите поставщика службы имен из списка.</span><span class="sxs-lookup"><span data-stu-id="78a66-128">In the **RPC Name Service Provider Configuration** dialog box, select a name service provider from the list.</span></span>
    1.  <span data-ttu-id="78a66-129">При выборе указателя Майкрософт нажмите кнопку ОК.</span><span class="sxs-lookup"><span data-stu-id="78a66-129">When you select Microsoft Locator, click OK.</span></span> <span data-ttu-id="78a66-130">После этого процесс настройки завершится.</span><span class="sxs-lookup"><span data-stu-id="78a66-130">The configuration process is then complete.</span></span>
    2.  <span data-ttu-id="78a66-131">При выборе службы каталогов ячеек DCE в поле **сетевой адрес** введите имя главного компьютера, на котором работает управляющая программа NSI (нсид), и нажмите кнопку ОК.</span><span class="sxs-lookup"><span data-stu-id="78a66-131">When you select the DCE Cell Directory Service, in the **Network Address** box, type the name of the host computer that runs the NSI daemon (nsid), and then click OK.</span></span>

 

 




