---
description: Wmiadap — это приложение, работающее в Windows, которое может обновлять сведения о производительности в репозитории WMI.
ms.assetid: 459fe19e-3e2e-4a58-b3e7-75fd285f7389
ms.tgt_platform: multiple
title: wmiadap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa5d2de65e8566283b341c5af52048cc79cc0299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272736"
---
# <a name="wmiadap"></a><span data-ttu-id="ce6c1-103">wmiadap</span><span class="sxs-lookup"><span data-stu-id="ce6c1-103">wmiadap</span></span>

<span data-ttu-id="ce6c1-104">Wmiadap — это приложение, работающее в Windows, которое может обновлять сведения о производительности в репозитории WMI.</span><span class="sxs-lookup"><span data-stu-id="ce6c1-104">Wmiadap is a application that runs on Windows that can update performance information in the WMI repository.</span></span> <span data-ttu-id="ce6c1-105">Как правило, это позволяет разработчикам и ИТ администраторам создавать сценарии, которые обращаются к сведениям о производительности, например объему памяти, используемому приложением.</span><span class="sxs-lookup"><span data-stu-id="ce6c1-105">Generally, this allows developers and IT Administrators to create scripts that access performance information, such as the amount of memory used by an application.</span></span> <span data-ttu-id="ce6c1-106">В следующем разделе описывается интерфейс командной строки, с помощью которого можно управлять получением информации wmiadap.</span><span class="sxs-lookup"><span data-stu-id="ce6c1-106">The following topic describes the command-line interface you can use to control how wmiadap retrieves information.</span></span>

<span data-ttu-id="ce6c1-107">Wmiadap устанавливается вместе с операционной системой в большинстве систем, в каталоге C: \\ Windows \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="ce6c1-107">Wmiadap is installed with the operating system on most systems, in the C:\\Windows\\System32\\wbem directory.</span></span> <span data-ttu-id="ce6c1-108">Если вы видите сообщения об ошибках, касающиеся wmiadap.exe, найдите [Служба поддержки Майкрософт](https://support.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="ce6c1-108">If you are seeing error messages concerning wmiadap.exe, search [Microsoft Support](https://support.microsoft.com/).</span></span> <span data-ttu-id="ce6c1-109">Как правило, не следует удалять wmiadap.exe из системы, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="ce6c1-109">Generally, you should not delete wmiadap.exe from your system, unless otherwise instructed.</span></span>

<span data-ttu-id="ce6c1-110">Перемещение данных из библиотек производительности и обновление классов, производных от [**Win32 \_ Перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) и [**Win32 \_ Перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) , осуществляется поставщиками [вмиперфкласс](wmi-providers.md) и [вмиперфинст](wmi-providers.md) .</span><span class="sxs-lookup"><span data-stu-id="ce6c1-110">The transfer of data from the performance libraries and the refresh of classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) is done by the [WmiPerfClass](wmi-providers.md) and [WMIPerfInst](wmi-providers.md) providers.</span></span> <span data-ttu-id="ce6c1-111">Поставщик Вмиперфкласс обновляет [Классы счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI только при добавлении нового объекта производительности.</span><span class="sxs-lookup"><span data-stu-id="ce6c1-111">The WmiPerfClass provider updates WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) only when a new performance object is added.</span></span> <span data-ttu-id="ce6c1-112">Вы по-прежнему можете запустить Wmiadap с параметром **/r** , чтобы проанализировать драйверы WDM для создания объектов производительности.</span><span class="sxs-lookup"><span data-stu-id="ce6c1-112">You still can run Wmiadap with the **/r** switch to parse the Windows Driver Model drivers to create performance objects.</span></span> <span data-ttu-id="ce6c1-113">Параметр **/f** по-прежнему вызывает обновление классов WMI из библиотек производительности.</span><span class="sxs-lookup"><span data-stu-id="ce6c1-113">The **/f** switch still forces an update of the WMI classes from the performance libraries.</span></span>

<span data-ttu-id="ce6c1-114">В командной строке доступны следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="ce6c1-114">The following switches are available at the command prompt.</span></span>

<span data-ttu-id="ce6c1-115">**wmiadap** \[  \] /f \[ **/r**\]</span><span class="sxs-lookup"><span data-stu-id="ce6c1-115">**wmiadap** \[**/f**\]\[**/r**\]</span></span>

## <a name="switches"></a><span data-ttu-id="ce6c1-116">коммутаторы;</span><span class="sxs-lookup"><span data-stu-id="ce6c1-116">Switches</span></span>

<dl> <dt>

<span data-ttu-id="ce6c1-117"><span id="_f"></span><span id="_F"></span>**ключа**</span><span class="sxs-lookup"><span data-stu-id="ce6c1-117"><span id="_f"></span><span id="_F"></span>**/f**</span></span>
</dt> <dd>

<span data-ttu-id="ce6c1-118">Анализирует все библиотеки производительности в системе и обновляет классы, производные от [**Win32 \_ Перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) и [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="ce6c1-118">Parses all the performance libraries on the system and refreshes the classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

</dd> <dt>

<span data-ttu-id="ce6c1-119"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="ce6c1-119"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="ce6c1-120">Анализирует все драйверы WDM в системе для создания объектов производительности.</span><span class="sxs-lookup"><span data-stu-id="ce6c1-120">Parses all the Windows Driver Model drivers on the system to create performance objects.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="ce6c1-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce6c1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce6c1-122">Библиотеки производительности и инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="ce6c1-122">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="ce6c1-123">**инициирует**</span><span class="sxs-lookup"><span data-stu-id="ce6c1-123">**winmgmt**</span></span>](winmgmt.md)
</dt> </dl>

 

 
