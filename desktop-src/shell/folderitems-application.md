---
description: Содержит объект приложения коллекции элементов папки.
ms.assetid: 2cd4243e-a5a6-4de4-b310-f74558ac0fbe
title: Свойство Фолдеритемс. Application (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7f073b81106923f889ca5209c0aa492f4c4bbd60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143036"
---
# <a name="folderitemsapplication-property"></a><span data-ttu-id="80b43-103">Фолдеритемс. Application, свойство</span><span class="sxs-lookup"><span data-stu-id="80b43-103">FolderItems.Application property</span></span>

<span data-ttu-id="80b43-104">Содержит объект **приложения** коллекции элементов папки.</span><span class="sxs-lookup"><span data-stu-id="80b43-104">Contains the **Application** object of the folder items collection.</span></span>

<span data-ttu-id="80b43-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="80b43-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="80b43-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80b43-106">Syntax</span></span>


```JScript
objApplication = FolderItems.Application
```



## <a name="property-value"></a><span data-ttu-id="80b43-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="80b43-107">Property value</span></span>

<span data-ttu-id="80b43-108">Ссылка на объект приложения.</span><span class="sxs-lookup"><span data-stu-id="80b43-108">An object reference to the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="80b43-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="80b43-109">Remarks</span></span>

<span data-ttu-id="80b43-110">Свойство **Application** возвращает объект автоматизации, поддерживаемый приложением, которое содержит элемент управления WebBrowser, если этот объект доступен.</span><span class="sxs-lookup"><span data-stu-id="80b43-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="80b43-111">В противном случае это свойство возвращает объект автоматизации элемента управления WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="80b43-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="80b43-112">Это свойство можно использовать с командами **Set** и **CreateObject** или с помощью команды **GetObject** для создания экземпляра приложения Windows Internet Explorer и управления им.</span><span class="sxs-lookup"><span data-stu-id="80b43-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="80b43-113">Требования</span><span class="sxs-lookup"><span data-stu-id="80b43-113">Requirements</span></span>



| <span data-ttu-id="80b43-114">Требование</span><span class="sxs-lookup"><span data-stu-id="80b43-114">Requirement</span></span> | <span data-ttu-id="80b43-115">Значение</span><span class="sxs-lookup"><span data-stu-id="80b43-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80b43-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80b43-116">Minimum supported client</span></span><br/> | <span data-ttu-id="80b43-117">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="80b43-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="80b43-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80b43-118">Minimum supported server</span></span><br/> | <span data-ttu-id="80b43-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="80b43-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="80b43-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="80b43-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="80b43-121"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="80b43-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="80b43-122">IDL</span><span class="sxs-lookup"><span data-stu-id="80b43-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="80b43-123"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="80b43-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="80b43-124">DLL</span><span class="sxs-lookup"><span data-stu-id="80b43-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80b43-125"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="80b43-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




