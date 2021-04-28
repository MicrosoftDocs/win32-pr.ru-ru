---
description: Shell. Application свойство — содержит объект приложения объекта.
ms.assetid: 5335f4dd-ca80-49c8-8953-e32a6e6308e0
title: Свойство Shell. Application (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5a90b3953ed54b8a3652d6c9c26533d433ffb600
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083862"
---
# <a name="shellapplication-property"></a><span data-ttu-id="d23f0-103">Свойство Shell. Application</span><span class="sxs-lookup"><span data-stu-id="d23f0-103">Shell.Application property</span></span>

<span data-ttu-id="d23f0-104">Содержит объект приложения объекта.</span><span class="sxs-lookup"><span data-stu-id="d23f0-104">Contains the object's Application object.</span></span>

<span data-ttu-id="d23f0-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d23f0-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d23f0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d23f0-106">Syntax</span></span>


```JScript
objApplication = Shell.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a><span data-ttu-id="d23f0-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d23f0-107">Property value</span></span>

<span data-ttu-id="d23f0-108">Переменная типа [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , которая получает объект приложения.</span><span class="sxs-lookup"><span data-stu-id="d23f0-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d23f0-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="d23f0-109">Remarks</span></span>

<span data-ttu-id="d23f0-110">Свойство **Application** возвращает объект автоматизации, поддерживаемый приложением, которое содержит элемент управления WebBrowser, если этот объект доступен.</span><span class="sxs-lookup"><span data-stu-id="d23f0-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="d23f0-111">В противном случае это свойство возвращает объект автоматизации элемента управления WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="d23f0-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="d23f0-112">Это свойство можно использовать с командами **Set** и **CreateObject** или с помощью команды **GetObject** для создания экземпляра приложения Windows Internet Explorer и управления им.</span><span class="sxs-lookup"><span data-stu-id="d23f0-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="d23f0-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d23f0-113">Requirements</span></span>



| <span data-ttu-id="d23f0-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d23f0-114">Requirement</span></span> | <span data-ttu-id="d23f0-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d23f0-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d23f0-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d23f0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d23f0-117">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d23f0-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d23f0-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d23f0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d23f0-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d23f0-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d23f0-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d23f0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d23f0-121"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="d23f0-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d23f0-122">IDL</span><span class="sxs-lookup"><span data-stu-id="d23f0-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d23f0-123"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d23f0-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d23f0-124">DLL</span><span class="sxs-lookup"><span data-stu-id="d23f0-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d23f0-125"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="d23f0-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
