---
description: Шеллфолдервиев. Application свойство — содержит объект приложения объекта.
ms.assetid: 305766b1-a19f-4743-a9e3-6837b3f8ffe0
title: Свойство Шеллфолдервиев. Application (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 95ef542f91235b3b068e1b1b54768b4dd453d9b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083472"
---
# <a name="shellfolderviewapplication-property"></a><span data-ttu-id="c33c1-103">Шеллфолдервиев. Application, свойство</span><span class="sxs-lookup"><span data-stu-id="c33c1-103">ShellFolderView.Application property</span></span>

<span data-ttu-id="c33c1-104">Содержит объект приложения объекта.</span><span class="sxs-lookup"><span data-stu-id="c33c1-104">Contains the object's Application object.</span></span>

<span data-ttu-id="c33c1-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c33c1-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c33c1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c33c1-106">Syntax</span></span>


```JScript
objApplication = ShellFolderView.Application
```



## <a name="property-value"></a><span data-ttu-id="c33c1-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c33c1-107">Property value</span></span>

<span data-ttu-id="c33c1-108">Переменная типа [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , которая получает объект приложения.</span><span class="sxs-lookup"><span data-stu-id="c33c1-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c33c1-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="c33c1-109">Remarks</span></span>

<span data-ttu-id="c33c1-110">Свойство **Application** возвращает объект автоматизации, поддерживаемый приложением, которое содержит элемент управления WebBrowser, если этот объект доступен.</span><span class="sxs-lookup"><span data-stu-id="c33c1-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="c33c1-111">В противном случае это свойство возвращает объект автоматизации элемента управления WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="c33c1-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="c33c1-112">Это свойство можно использовать с командами **Set** и **CreateObject** или с помощью команды **GetObject** для создания экземпляра приложения Windows Internet Explorer и управления им.</span><span class="sxs-lookup"><span data-stu-id="c33c1-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="c33c1-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c33c1-113">Requirements</span></span>



| <span data-ttu-id="c33c1-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c33c1-114">Requirement</span></span> | <span data-ttu-id="c33c1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c33c1-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c33c1-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c33c1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c33c1-117">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c33c1-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c33c1-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c33c1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c33c1-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c33c1-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c33c1-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c33c1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c33c1-121"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="c33c1-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c33c1-122">IDL</span><span class="sxs-lookup"><span data-stu-id="c33c1-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c33c1-123"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c33c1-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c33c1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c33c1-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c33c1-125"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="c33c1-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
