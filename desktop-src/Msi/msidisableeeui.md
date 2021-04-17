---
description: Чтобы отключить внедренный пользовательский интерфейс для установки, определенной в таблице Мсиембеддедуи, установите для свойства МСИДИСАБЛИЕУИ значение 1 в командной строке.
ms.assetid: c5ada690-c5dd-455f-babe-8c09750525c4
title: МСИДИСАБЛИЕУИ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d89ce43f649d406e4ae086db236375c02c43e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668729"
---
# <a name="msidisableeeui-property"></a><span data-ttu-id="db4f2-103">МСИДИСАБЛИЕУИ, свойство</span><span class="sxs-lookup"><span data-stu-id="db4f2-103">MSIDISABLEEEUI property</span></span>

<span data-ttu-id="db4f2-104">Чтобы отключить внедренный пользовательский интерфейс для установки, определенной в [таблице мсиембеддедуи](msiembeddedui-table.md), установите для свойства мсидисаблиеуи значение 1 в командной строке.</span><span class="sxs-lookup"><span data-stu-id="db4f2-104">To disable the embedded user interface for the installation defined in the [MsiEmbeddedUI table](msiembeddedui-table.md), set the MSIDISABLEEEUI property to 1 on the command line.</span></span>

<span data-ttu-id="db4f2-105">**[Установщик Windows 4,0 и более ранних версий](not-supported-in-windows-installer-4-0.md):** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="db4f2-105">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="db4f2-106">Версии, предшествующие установщик Windows 4,5, игнорируют свойство МСИДИСАБЛИЕУИ.</span><span class="sxs-lookup"><span data-stu-id="db4f2-106">Versions earlier than Windows Installer 4.5 ignore the MSIDISABLEEEUI Property.</span></span>

## <a name="remarks"></a><span data-ttu-id="db4f2-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="db4f2-107">Remarks</span></span>

<span data-ttu-id="db4f2-108">При установке нескольких пакетов дочерний пакет обычно использует пользовательский интерфейс родительского пакета и не инициализирует собственный встроенный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="db4f2-108">In a multiple-package installation, a child package should typically use the user interface of the parent package and not initialize its own embedded UI.</span></span> <span data-ttu-id="db4f2-109">Если свойство МСИДИСАБЛИЕУИ не задано в родительском пакете, дочерний пакет по умолчанию использует внедренный пользовательский интерфейс родительского пакета и игнорирует свойство МСИДИСАБЛИЕУИ в дочернем пакете.</span><span class="sxs-lookup"><span data-stu-id="db4f2-109">If the MSIDISABLEEEUI property is not set inside the parent package, the child package uses the embedded UI of the parent package by default and ignores the MSIDISABLEEEUI property within the child package.</span></span>

<span data-ttu-id="db4f2-110">Свойство МСИДИСАБЛИЕУИ отключает внедренный пользовательский интерфейс для одного пакета.</span><span class="sxs-lookup"><span data-stu-id="db4f2-110">The MSIDISABLEEEUI property disables the embedded user interface for a single package.</span></span> <span data-ttu-id="db4f2-111">Вы можете использовать политику [мсидисаблимбеддедуи](msidisableembeddedui.md) , чтобы отключить встроенные пользовательские интерфейсы для всех пакетов на компьютере.</span><span class="sxs-lookup"><span data-stu-id="db4f2-111">You can use the [MsiDisableEmbeddedUI](msidisableembeddedui.md) policy to disable embedded user interfaces for all packages on the computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="db4f2-112">Требования</span><span class="sxs-lookup"><span data-stu-id="db4f2-112">Requirements</span></span>



| <span data-ttu-id="db4f2-113">Требование</span><span class="sxs-lookup"><span data-stu-id="db4f2-113">Requirement</span></span> | <span data-ttu-id="db4f2-114">Значение</span><span class="sxs-lookup"><span data-stu-id="db4f2-114">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db4f2-115">Версия</span><span class="sxs-lookup"><span data-stu-id="db4f2-115">Version</span></span><br/> | <span data-ttu-id="db4f2-116">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="db4f2-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="db4f2-117">Установщик Windows 4,5 в Windows Server 2008, Windows Vista, Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="db4f2-117">Windows Installer 4.5 on Windows Server 2008, Windows Vista, Windows Server 2003, and Windows XP.</span></span> <span data-ttu-id="db4f2-118">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="db4f2-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="db4f2-119">См. также</span><span class="sxs-lookup"><span data-stu-id="db4f2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db4f2-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="db4f2-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




