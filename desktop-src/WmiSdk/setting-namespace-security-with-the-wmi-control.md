---
description: Элемент управления WMI является оснасткой консоли MMC, расположенной на панели управления, и используется для установки безопасности пространства имен WMI вручную на локальном компьютере. Можно также задать пространство имен по умолчанию для сценариев.
ms.assetid: 87c23919-c482-4278-b005-894a8ac21da4
ms.tgt_platform: multiple
title: Настройка безопасности пространства имен с помощью элемента управления WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8e8b6ed7c45b6b0d107f7f4e4b92f31f504900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703175"
---
# <a name="setting-namespace-security-with-the-wmi-control"></a><span data-ttu-id="bf638-104">Настройка безопасности пространства имен с помощью элемента управления WMI</span><span class="sxs-lookup"><span data-stu-id="bf638-104">Setting Namespace Security with the WMI Control</span></span>

<span data-ttu-id="bf638-105">Элемент управления WMI является оснасткой консоли MMC, расположенной на **панели управления** , и используется для установки безопасности пространства имен WMI вручную на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="bf638-105">The WMI Control is an MMC snap-in located in the **Control Panel** and is used to set WMI namespace security manually on a local computer.</span></span> <span data-ttu-id="bf638-106">Можно также задать пространство имен по умолчанию для сценариев.</span><span class="sxs-lookup"><span data-stu-id="bf638-106">You can also set the default namespace for scripting.</span></span>


<span data-ttu-id="bf638-107">В следующей процедуре описывается, как разместить элемент управления WMI.</span><span class="sxs-lookup"><span data-stu-id="bf638-107">The following procedure describes how to locate the WMI Control.</span></span>

<span data-ttu-id="bf638-108">**Определение местоположения элемента управления WMI**</span><span class="sxs-lookup"><span data-stu-id="bf638-108">**To locate the WMI control**</span></span>

1.  <span data-ttu-id="bf638-109">На **панели управления** дважды щелкните **Администрирование**.</span><span class="sxs-lookup"><span data-stu-id="bf638-109">In the **Control Panel**, double-click **Administrative Tools**.</span></span>
2.  <span data-ttu-id="bf638-110">В окне **Администрирование** дважды щелкните **Управление компьютером**.</span><span class="sxs-lookup"><span data-stu-id="bf638-110">In the **Administrative Tools** window, double-click **Computer Management**.</span></span>
3.  <span data-ttu-id="bf638-111">В окне **Управление компьютером** разверните дерево **службы и приложения** и дважды щелкните **элемент управления WMI**.</span><span class="sxs-lookup"><span data-stu-id="bf638-111">In the **Computer Management** window, expand the **Services and Applications** tree and double-click the **WMI Control**.</span></span>
4.  <span data-ttu-id="bf638-112">Щелкните правой кнопкой мыши значок **элемента управления WMI** и выберите пункт **свойства**.</span><span class="sxs-lookup"><span data-stu-id="bf638-112">Right-click the **WMI Control** icon and select **Properties**.</span></span>

<span data-ttu-id="bf638-113">В следующей процедуре описывается использование элемента управления WMI для настройки безопасности пространства имен в качестве шаблона, а затем программное получение параметров безопасности для настройки безопасности других пространств имен.</span><span class="sxs-lookup"><span data-stu-id="bf638-113">The following procedure describes how to use the WMI control to set up the security for a namespace as a template, then programmatically obtain the security settings to set security for other namespaces.</span></span>

<span data-ttu-id="bf638-114">**Настройка безопасности пространства имен с помощью элемента управления WMI**</span><span class="sxs-lookup"><span data-stu-id="bf638-114">**To set namespace security with the WMI control**</span></span>

1.  <span data-ttu-id="bf638-115">Создайте новое пространство имен с помощью кода MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="bf638-115">Create a new namespace by using Managed Object Format (MOF) code.</span></span>
2.  <span data-ttu-id="bf638-116">Запустите элемент управления WMI, чтобы настроить безопасность для нового пространства имен.</span><span class="sxs-lookup"><span data-stu-id="bf638-116">Run the WMI Control to set the security on the new namespace.</span></span> <span data-ttu-id="bf638-117">В меню **Пуск** выберите пункт **выполнить** и введите **wmimgmt. msc** или см. раздел [Поиск элемента управления WMI](#).</span><span class="sxs-lookup"><span data-stu-id="bf638-117">On the **Start** menu, click **Run** and type **wmimgmt.msc** or see [Locating the WMI Control](#).</span></span>
3.  <span data-ttu-id="bf638-118">На панели **управления WMI** щелкните правой кнопкой мыши **элемент Управление WMI**, выберите пункт **Свойства**, а затем перейдите на вкладку **Безопасность** .</span><span class="sxs-lookup"><span data-stu-id="bf638-118">In the **WMI Control** pane, right-click **WMI Control**, choose **Properties**, and then select the **Security** tab.</span></span>
4.  <span data-ttu-id="bf638-119">Перейдите к новому пространству имен, щелкните **Безопасность**, а затем настройте группы и разрешения для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="bf638-119">Navigate to the new namespace, click **Security**, and then configure groups and permissions for the namespace.</span></span>

<span data-ttu-id="bf638-120">Для настройки безопасности пространства имен можно также использовать инструментарий управления Windows (WMI) Command-Line ([WMIC](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754534(v=ws.11))).</span><span class="sxs-lookup"><span data-stu-id="bf638-120">You can also use Windows Management Instrumentation Command-Line ([WMIC](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754534(v=ws.11))) to set namespace security.</span></span> <span data-ttu-id="bf638-121">Дополнительные сведения см. в разделе [**WMIC**](wmic.md).</span><span class="sxs-lookup"><span data-stu-id="bf638-121">For more information, see [**wmic**](wmic.md).</span></span>

## <a name="setting-the-default-namespace-for-scripts"></a><span data-ttu-id="bf638-122">Задание пространства имен по умолчанию для скриптов</span><span class="sxs-lookup"><span data-stu-id="bf638-122">Setting the Default Namespace for Scripts</span></span>

<span data-ttu-id="bf638-123">Если скрипт не подключается явно к пространству имен при подключении к WMI, WMI использует пространство имен по умолчанию, заданное в этом элементе управления.</span><span class="sxs-lookup"><span data-stu-id="bf638-123">If a script does not connect explicitly to a namespace when connecting to WMI, then WMI uses the default namespace specified in this control.</span></span> <span data-ttu-id="bf638-124">Значение по умолчанию также находится в записи реестра следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bf638-124">The default is also found in the registry entry as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         WBEM
            Scripting
               Default
                  Namespace
```

<span data-ttu-id="bf638-125">Поскольку пространство имен по умолчанию легко изменить с помощью этого элемента управления или программным путем, вызывая методы [**стдрегпров**](/previous-versions/windows/desktop/regprov/stdregprov), укажите пространство имен при соединении с WMI с помощью [моникера](constructing-a-moniker-string.md) или вызовов [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md).</span><span class="sxs-lookup"><span data-stu-id="bf638-125">Because the default namespace is easy to change, either with this control or programmatically by calling methods of [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), specify the namespace when connecting to WMI either through the [moniker](constructing-a-moniker-string.md) or calls to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span> <span data-ttu-id="bf638-126">Дополнительные сведения см. [в разделе Создание скрипта WMI](creating-a-wmi-script.md) .</span><span class="sxs-lookup"><span data-stu-id="bf638-126">For more information, see [Creating a WMI Script](creating-a-wmi-script.md)</span></span>

<span data-ttu-id="bf638-127">**Задание пространства имен по умолчанию для скриптов**</span><span class="sxs-lookup"><span data-stu-id="bf638-127">**To set the default namespace for scripts**</span></span>

1.  <span data-ttu-id="bf638-128">В окне **свойства элемента управления WMI** перейдите на вкладку **Дополнительно** .</span><span class="sxs-lookup"><span data-stu-id="bf638-128">In the **WMI Control Properties** window, choose the **Advanced** tab.</span></span>
2.  <span data-ttu-id="bf638-129">Нажмите кнопку **изменить** и выберите пространство имен, чтобы использовать его по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bf638-129">Click the **Change** button and select the namespace to make the default.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf638-130">См. также</span><span class="sxs-lookup"><span data-stu-id="bf638-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf638-131">Задание дескрипторов безопасности пространства имен</span><span class="sxs-lookup"><span data-stu-id="bf638-131">Setting Namespace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> </dl>

 

 
