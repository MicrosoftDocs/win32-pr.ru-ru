---
description: Содержит объект приложения для элемента папки.
ms.assetid: cd8d6dea-1d16-4d62-b56b-c915192f730b
title: Свойство FolderItem. Application (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 72816ed0c426f6ff3fa92c30a1ec31757c0a02fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539518"
---
# <a name="folderitemapplication-property"></a><span data-ttu-id="7abac-103">FolderItem. Application, свойство</span><span class="sxs-lookup"><span data-stu-id="7abac-103">FolderItem.Application property</span></span>

<span data-ttu-id="7abac-104">Содержит объект **приложения** для элемента папки.</span><span class="sxs-lookup"><span data-stu-id="7abac-104">Contains the **Application** object of the folder item.</span></span>

<span data-ttu-id="7abac-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7abac-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7abac-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7abac-106">Syntax</span></span>


```JScript
objApplication = FolderItem.Application
```



## <a name="property-value"></a><span data-ttu-id="7abac-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7abac-107">Property value</span></span>

<span data-ttu-id="7abac-108">Переменная типа [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , которая получает объект **приложения** .</span><span class="sxs-lookup"><span data-stu-id="7abac-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the **Application** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7abac-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="7abac-109">Remarks</span></span>

<span data-ttu-id="7abac-110">Свойство **Application** возвращает объект автоматизации, поддерживаемый приложением, которое содержит элемент управления WebBrowser, если этот объект доступен.</span><span class="sxs-lookup"><span data-stu-id="7abac-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="7abac-111">В противном случае это свойство возвращает объект автоматизации элемента управления WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="7abac-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="7abac-112">Это свойство можно использовать с командами **Set** и **CreateObject** или с помощью команды **GetObject** для создания экземпляра приложения Windows Internet Explorer и управления им.</span><span class="sxs-lookup"><span data-stu-id="7abac-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="7abac-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7abac-113">Requirements</span></span>



| <span data-ttu-id="7abac-114">Требование</span><span class="sxs-lookup"><span data-stu-id="7abac-114">Requirement</span></span> | <span data-ttu-id="7abac-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7abac-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7abac-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7abac-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7abac-117">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7abac-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7abac-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7abac-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7abac-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7abac-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7abac-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7abac-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7abac-121"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="7abac-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7abac-122">IDL</span><span class="sxs-lookup"><span data-stu-id="7abac-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7abac-123"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7abac-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7abac-124">DLL</span><span class="sxs-lookup"><span data-stu-id="7abac-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7abac-125"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="7abac-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
