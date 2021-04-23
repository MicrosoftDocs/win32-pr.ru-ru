---
description: Программисты используют технологии авторизации для создания программного обеспечения управления доступом, контроля доступа к Интернету, контроля доступа к безопасности и защиты файлов.
ms.assetid: 1b8306da-7577-40b8-b77c-5762c1962f00
title: Авторизация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c939a4dd8747b7219fe99650ab7a078239b5f643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104273105"
---
# <a name="authorization"></a><span data-ttu-id="e737a-103">Авторизация</span><span class="sxs-lookup"><span data-stu-id="e737a-103">Authorization</span></span>

## <a name="purpose"></a><span data-ttu-id="e737a-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="e737a-104">Purpose</span></span>

<span data-ttu-id="e737a-105">Авторизация — это право, предоставленное пользователю для использования системы и хранящихся в ней данных.</span><span class="sxs-lookup"><span data-stu-id="e737a-105">Authorization is the right granted an individual to use the system and the data stored on it.</span></span> <span data-ttu-id="e737a-106">Авторизация обычно настраивается системным администратором и проверяется компьютером с учетом определенной формы идентификации пользователя, например номера кода или пароля.</span><span class="sxs-lookup"><span data-stu-id="e737a-106">Authorization is typically set up by a system administrator and verified by the computer based on some form of user identification, such as a code number or password.</span></span>

<span data-ttu-id="e737a-107">Технологии авторизации Майкрософт включают в себя диспетчер авторизации и API-интерфейс authz.</span><span class="sxs-lookup"><span data-stu-id="e737a-107">Microsoft authorization technologies include Authorization Manager and the Authz API.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="e737a-108">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="e737a-108">Developer audience</span></span>

<span data-ttu-id="e737a-109">Технологии авторизации Майкрософт предназначены для разработчиков приложений, основанных на операционных системах Windows Server и Windows, которые контролируют доступ к ресурсам.</span><span class="sxs-lookup"><span data-stu-id="e737a-109">Microsoft authorization technologies are intended for use by developers of applications based on the Windows Server and Windows operating systems that control access to resources.</span></span> <span data-ttu-id="e737a-110">Разработчики должны быть знакомы с программированием на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="e737a-110">Developers should be familiar with Windows-based programming.</span></span> <span data-ttu-id="e737a-111">Хотя это и не является обязательным, рекомендуется понимание субъектов, относящихся к авторизации или безопасности.</span><span class="sxs-lookup"><span data-stu-id="e737a-111">Although not required, an understanding of authorization or security-related subjects is advised.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="e737a-112">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="e737a-112">Run-time requirements</span></span>

<span data-ttu-id="e737a-113">Сведения о требованиях времени выполнения для определенного программного элемента см. в разделе "требования" на странице справочника по этому элементу.</span><span class="sxs-lookup"><span data-stu-id="e737a-113">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e737a-114">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="e737a-114">In this section</span></span>



| <span data-ttu-id="e737a-115">Раздел</span><span class="sxs-lookup"><span data-stu-id="e737a-115">Topic</span></span>                                                             | <span data-ttu-id="e737a-116">Описание</span><span class="sxs-lookup"><span data-stu-id="e737a-116">Description</span></span>                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e737a-117">Об авторизации</span><span class="sxs-lookup"><span data-stu-id="e737a-117">About Authorization</span></span>](about-authorization.md)<br/>         | <span data-ttu-id="e737a-118">Основные понятия авторизации и высокоуровневое представление технологий авторизации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="e737a-118">Key authorization concepts and a high-level view of Microsoft authorization technologies.</span></span><br/>                                                                                                                                                                                  |
| <span data-ttu-id="e737a-119">Использование авторизации</span><span class="sxs-lookup"><span data-stu-id="e737a-119">Using Authorization</span></span><br/>                                    | <span data-ttu-id="e737a-120">Процессы авторизации, процедуры и примеры программ, использующих технологии авторизации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="e737a-120">Authorization processes, procedures, and examples of programs using Microsoft authorization technologies.</span></span> <span data-ttu-id="e737a-121">Эти сведения представлены в разделе использование языков программирования [C++](using-authorization-in-c--.md) и [скриптов](using-authorization-in-script.md) .</span><span class="sxs-lookup"><span data-stu-id="e737a-121">This information is presented in using sections for [C++](using-authorization-in-c--.md) and [Script](using-authorization-in-script.md) programming languages.</span></span><br/> |
| [<span data-ttu-id="e737a-122">Справочник по авторизации</span><span class="sxs-lookup"><span data-stu-id="e737a-122">Authorization Reference</span></span>](authorization-reference.md)<br/> | <span data-ttu-id="e737a-123">Подробные сведения о функциях авторизации, интерфейсах, структурах и других программных элементах.</span><span class="sxs-lookup"><span data-stu-id="e737a-123">Detailed information about authorization functions, interfaces, structures, and other programming elements.</span></span><br/>                                                                                                                                                                |



 

 

 




