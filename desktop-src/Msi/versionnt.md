---
description: Установщик задает для свойства Версионнт номер версии операционной системы, а не определен, если операционная система не является Windows NT, Windows 2000, Windows XP, Windows Vista, Windows Server 2008 или Windows 7.
ms.assetid: 49005783-0bcb-458e-8266-56e6ea6afb43
title: Версионнт, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61ce8d7d5c738be3b2fd51f2ca3054b8800d4c40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651942"
---
# <a name="versionnt-property"></a><span data-ttu-id="7fdb5-103">Версионнт, свойство</span><span class="sxs-lookup"><span data-stu-id="7fdb5-103">VersionNT property</span></span>

<span data-ttu-id="7fdb5-104">Установщик задает для свойства **версионнт** номер версии операционной системы, а не определен, если операционная система не является Windows NT, Windows 2000, Windows XP, Windows Vista, windows Server 2008 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7fdb5-104">The installer sets the **VersionNT** property to the version number for the operating system, undefined if the operating system is not Windows NT, Windows 2000, Windows XP, Windows Vista, Windows Server 2008, or Windows 7.</span></span> <span data-ttu-id="7fdb5-105">Значение является целым числом: MajorVersion \* 100 + minorversion.</span><span class="sxs-lookup"><span data-stu-id="7fdb5-105">The value is an integer: MajorVersion \* 100 + MinorVersion.</span></span>

<span data-ttu-id="7fdb5-106">Это свойство может использоваться в условных инструкциях, зависящих от операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7fdb5-106">Conditional statements that depend upon the operating system can use this property.</span></span>

<span data-ttu-id="7fdb5-107">См. также [значения свойств операционной системы](operating-system-property-values.md).</span><span class="sxs-lookup"><span data-stu-id="7fdb5-107">See also [Operating System Property Values](operating-system-property-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7fdb5-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7fdb5-108">Remarks</span></span>

<span data-ttu-id="7fdb5-109">Выражения условий могут протестировать Windows NT, Windows 2000 или Windows XP с помощью имени свойства или проверить версию с помощью оператора сравнения.</span><span class="sxs-lookup"><span data-stu-id="7fdb5-109">Condition expressions can test for Windows NT, Windows 2000, or Windows XP by using the property name, or may verify the version by using a comparison operator.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fdb5-110">Требования</span><span class="sxs-lookup"><span data-stu-id="7fdb5-110">Requirements</span></span>



| <span data-ttu-id="7fdb5-111">Требование</span><span class="sxs-lookup"><span data-stu-id="7fdb5-111">Requirement</span></span> | <span data-ttu-id="7fdb5-112">Значение</span><span class="sxs-lookup"><span data-stu-id="7fdb5-112">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fdb5-113">Версия</span><span class="sxs-lookup"><span data-stu-id="7fdb5-113">Version</span></span><br/> | <span data-ttu-id="7fdb5-114">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7fdb5-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7fdb5-115">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7fdb5-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7fdb5-116">Установщик Windows в Windows Server 2003 или Windows XP ознакомьтесь с [требованиями к установщик Windows Run-Time](windows-installer-portal.md) , чтобы получить сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии.</span><span class="sxs-lookup"><span data-stu-id="7fdb5-116">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7fdb5-117">См. также</span><span class="sxs-lookup"><span data-stu-id="7fdb5-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fdb5-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="7fdb5-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 




