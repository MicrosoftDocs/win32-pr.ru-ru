---
description: 'Свойство Time — это текущее время в часах, минутах и секундах в виде строки литерального текста в формате чч: мм: СС с использованием 24-часового времени.'
ms.assetid: 6f487e46-e178-4d41-b6fa-7c16aa1c46fd
title: Свойство Time
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10c3456063842c8dd89fadf5860733b5c5aecbef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675873"
---
# <a name="time-property"></a><span data-ttu-id="2ca3d-103">Свойство Time</span><span class="sxs-lookup"><span data-stu-id="2ca3d-103">Time property</span></span>

<span data-ttu-id="2ca3d-104">Свойство **time** — это текущее время в часах, минутах и секундах в виде строки литерального текста в формате чч: мм: СС с использованием 24-часового времени.</span><span class="sxs-lookup"><span data-stu-id="2ca3d-104">The **Time** property is the current time in hours, minutes, and seconds as a string of literal text in the format HH:MM:SS using a 24 hour clock.</span></span> <span data-ttu-id="2ca3d-105">Например, время 6:57 вечера.</span><span class="sxs-lookup"><span data-stu-id="2ca3d-105">For example, the time 6:57 p.m.</span></span> <span data-ttu-id="2ca3d-106">представляется "18:57:00".</span><span class="sxs-lookup"><span data-stu-id="2ca3d-106">is represented by "18:57:00".</span></span> <span data-ttu-id="2ca3d-107">Формат значения зависит от языкового стандарта пользователя и имеет формат, полученный с помощью функции [**жеттимеформат**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) с \_ \| параметром времени FORCE24HOURFORMAT времени \_ нотимемаркер.</span><span class="sxs-lookup"><span data-stu-id="2ca3d-107">The format of the value depends upon the user's locale, and is the format obtained using [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) function with the TIME\_FORCE24HOURFORMAT \| TIME\_NOTIMEMARKER option.</span></span> <span data-ttu-id="2ca3d-108">Значение этого свойства задается установщик Windows, а не автором пакета.</span><span class="sxs-lookup"><span data-stu-id="2ca3d-108">The value of this property is set by the Windows Installer and not the package author.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ca3d-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2ca3d-109">Remarks</span></span>

<span data-ttu-id="2ca3d-110">Поскольку это текстовая строка, ее нельзя использовать в условных выражениях.</span><span class="sxs-lookup"><span data-stu-id="2ca3d-110">Because this is a text string, it cannot be used in conditional expressions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ca3d-111">Требования</span><span class="sxs-lookup"><span data-stu-id="2ca3d-111">Requirements</span></span>



| <span data-ttu-id="2ca3d-112">Требование</span><span class="sxs-lookup"><span data-stu-id="2ca3d-112">Requirement</span></span> | <span data-ttu-id="2ca3d-113">Значение</span><span class="sxs-lookup"><span data-stu-id="2ca3d-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca3d-114">Версия</span><span class="sxs-lookup"><span data-stu-id="2ca3d-114">Version</span></span><br/> | <span data-ttu-id="2ca3d-115">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2ca3d-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2ca3d-116">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2ca3d-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2ca3d-117">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2ca3d-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="2ca3d-118">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="2ca3d-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2ca3d-119">См. также</span><span class="sxs-lookup"><span data-stu-id="2ca3d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ca3d-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="2ca3d-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 
