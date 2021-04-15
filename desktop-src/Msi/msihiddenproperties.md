---
description: Свойство Мсихидденпропертиес может использоваться, чтобы запретить установщику выводить пароли или другие конфиденциальные сведения в файле журнала.
ms.assetid: 7d5eb9cf-04a5-41bd-9ca9-f30af45ab0a5
title: Мсихидденпропертиес, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6124f7002edd8ab7d3d5e6691b7b0a322b93c285
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668719"
---
# <a name="msihiddenproperties-property"></a><span data-ttu-id="f5e21-103">Мсихидденпропертиес, свойство</span><span class="sxs-lookup"><span data-stu-id="f5e21-103">MsiHiddenProperties property</span></span>

<span data-ttu-id="f5e21-104">Свойство **мсихидденпропертиес** может использоваться, чтобы запретить установщику выводить пароли или другие конфиденциальные сведения в файле журнала.</span><span class="sxs-lookup"><span data-stu-id="f5e21-104">The **MsiHiddenProperties** property may be used to prevent the installer from displaying passwords or other confidential information in the log file.</span></span> <span data-ttu-id="f5e21-105">Чтобы предотвратить запись свойства в файл журнала, присвойте свойству **мсихидденпропертиес** имя свойства, которое необходимо скрыть.</span><span class="sxs-lookup"><span data-stu-id="f5e21-105">To prevent a property from being written into the log file, set the value of the **MsiHiddenProperties** property to the name of the property you wish to hide.</span></span> <span data-ttu-id="f5e21-106">Можно скрыть несколько свойств, указав строку имен свойств, разделенную точкой с запятой (;).</span><span class="sxs-lookup"><span data-stu-id="f5e21-106">You can hide multiple properties by specifying a string of property names delimited by semicolons (;).</span></span>

> [!Note]  
> <span data-ttu-id="f5e21-107">Если для политики [отладки](debug.md) задано значение 7, установщик будет записывать в журнал сведения, указанные в командной строке.</span><span class="sxs-lookup"><span data-stu-id="f5e21-107">When the [Debug](debug.md) policy is set to a value of 7, the installer will write information entered on a command line into the log.</span></span> <span data-ttu-id="f5e21-108">Это делает открытые свойства, введенные в командную строку, видимыми даже в том случае, если свойство включено в свойство **мсихидденпропертиес** .</span><span class="sxs-lookup"><span data-stu-id="f5e21-108">This makes public properties entered on a command line visible even if the property is included in the **MsiHiddenProperties** property.</span></span> <span data-ttu-id="f5e21-109">Это может привести к добавлению конфиденциальной информации в командную строку, видимую в журнале.</span><span class="sxs-lookup"><span data-stu-id="f5e21-109">This can make confidential information entered on a command line visible in the log.</span></span> <span data-ttu-id="f5e21-110">Дополнительные сведения см. в разделе [предотвращение записи конфиденциальной информации в файл журнала](preventing-confidential-information-from-being-written-into-the-log-file.md).</span><span class="sxs-lookup"><span data-stu-id="f5e21-110">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f5e21-111">Требования</span><span class="sxs-lookup"><span data-stu-id="f5e21-111">Requirements</span></span>



| <span data-ttu-id="f5e21-112">Требование</span><span class="sxs-lookup"><span data-stu-id="f5e21-112">Requirement</span></span> | <span data-ttu-id="f5e21-113">Значение</span><span class="sxs-lookup"><span data-stu-id="f5e21-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5e21-114">Версия</span><span class="sxs-lookup"><span data-stu-id="f5e21-114">Version</span></span><br/> | <span data-ttu-id="f5e21-115">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f5e21-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f5e21-116">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f5e21-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f5e21-117">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f5e21-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="f5e21-118">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="f5e21-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f5e21-119">См. также</span><span class="sxs-lookup"><span data-stu-id="f5e21-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5e21-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="f5e21-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




