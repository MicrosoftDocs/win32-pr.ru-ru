---
description: После завершения работы с классом или экземпляром может потребоваться удалить этот класс или экземпляр из WMI.
ms.assetid: 8d4bf548-a332-4058-92d0-d613bbeaa408
ms.tgt_platform: multiple
title: Удаление класса или экземпляра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42a46a52400623e31df3e051a0b587f49326733b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263935"
---
# <a name="deleting-a-class-or-instance"></a><span data-ttu-id="5dd3e-103">Удаление класса или экземпляра</span><span class="sxs-lookup"><span data-stu-id="5dd3e-103">Deleting a Class or Instance</span></span>

<span data-ttu-id="5dd3e-104">После завершения работы с классом или экземпляром может потребоваться удалить этот класс или экземпляр из WMI.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-104">After you finish with a class or an instance, you may wish to delete that class or instance from WMI.</span></span> <span data-ttu-id="5dd3e-105">Как и другие объектно-ориентированные технологии, можно удалить объекты класса или экземпляра, чтобы очистить пространство имен WMI и вернуть системные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-105">Like other object-oriented technologies, you can delete class or instance objects to clean up the WMI namespace and to return system resources.</span></span> <span data-ttu-id="5dd3e-106">Однако многие классы и экземпляры в WMI являются постоянными и используются различными приложениями в любой момент времени, поэтому следует соблюдать осторожность при удалении класса или экземпляра WMI: приложение или другое приложение, скорее всего, потребуют класс или экземпляр позже.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-106">However, many classes and instances in WMI are persistent and are used by a variety of applications at any given time Therefore, you should be careful when deleting a WMI class or instance: your application or another application will probably need the class or instance at a later date.</span></span>

<span data-ttu-id="5dd3e-107">Удаление класса или экземпляра является простой процедурой.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-107">Deleting a class or an instance is a simple procedure.</span></span> <span data-ttu-id="5dd3e-108">Однако из-за постоянной природы класса вам, возможно, не придется удалять класс часто.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-108">However, due to the permanent nature of a class, you will probably not need to delete a class often.</span></span> <span data-ttu-id="5dd3e-109">Например, маловероятно удалить класс [**Win32 \_ дискдриве**](/windows/desktop/CIMWin32Prov/win32-diskdrive) , так как маловероятно, что в вашей организации нет диска.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-109">For example, you are unlikely to delete the [**Win32\_DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) class, because it is unlikely that you do not have a disk drive somewhere in your enterprise.</span></span> <span data-ttu-id="5dd3e-110">Вместо этого, скорее всего, будет удален экземпляр класса.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-110">Instead, you will be more likely to delete an instance of a class.</span></span> <span data-ttu-id="5dd3e-111">Дополнительные сведения см. в разделе [Удаление экземпляра](deleting-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="5dd3e-111">For more information, see [Deleting an Instance](deleting-an-instance.md).</span></span>

<span data-ttu-id="5dd3e-112">Хотя это и редко, вы можете полагаться на время, когда нужно обновить созданный класс.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-112">Although uncommon, you may come across a time where you wish to update a class that you created.</span></span> <span data-ttu-id="5dd3e-113">Например, можно создать класс для представления приложения стороннего производителя.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-113">For example, you could create a class to represent a third-party application.</span></span> <span data-ttu-id="5dd3e-114">Если программное обеспечение стороннего производителя обновило в ту область, в которой ваш класс больше не представляет программное обеспечение, может потребоваться удалить исходный класс.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-114">If the third-party updated their software to the extent that your class no longer properly represented the software, you may need to delete your original class.</span></span> <span data-ttu-id="5dd3e-115">Дополнительные сведения см. [в разделе Удаление класса](deleting-a-class.md).</span><span class="sxs-lookup"><span data-stu-id="5dd3e-115">For more information, see [Deleting a Class](deleting-a-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5dd3e-116">См. также</span><span class="sxs-lookup"><span data-stu-id="5dd3e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5dd3e-117">Разработка классов MOF-файл (MOF)</span><span class="sxs-lookup"><span data-stu-id="5dd3e-117">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
