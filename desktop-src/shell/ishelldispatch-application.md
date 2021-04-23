---
description: Содержит объект, представляющий приложение.
ms.assetid: 61B85691-399D-41c1-9901-825345A38E5A
title: Свойство Ишеллдиспатч. Application (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5adeb5663220309310c7cccb323be877de909516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543167"
---
# <a name="ishelldispatchapplication-property"></a><span data-ttu-id="3c400-103">Ишеллдиспатч. Application, свойство</span><span class="sxs-lookup"><span data-stu-id="3c400-103">IShellDispatch.Application property</span></span>

<span data-ttu-id="3c400-104">Содержит объект, представляющий приложение.</span><span class="sxs-lookup"><span data-stu-id="3c400-104">Contains an object that represents an application.</span></span>

<span data-ttu-id="3c400-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3c400-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c400-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c400-106">Syntax</span></span>


```JScript
objApplication = IShellDispatch.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a><span data-ttu-id="3c400-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3c400-107">Property value</span></span>

<span data-ttu-id="3c400-108">Переменная типа [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , которая получает объект приложения.</span><span class="sxs-lookup"><span data-stu-id="3c400-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c400-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="3c400-109">Remarks</span></span>

<span data-ttu-id="3c400-110">Это свойство реализовано и доступно через свойство [**Shell. ежектпк**](shell-ejectpc.md) .</span><span class="sxs-lookup"><span data-stu-id="3c400-110">This property is implemented and accessed through the [**Shell.EjectPC**](shell-ejectpc.md) property.</span></span>

<span data-ttu-id="3c400-111">Свойство **Application** возвращает объект автоматизации, поддерживаемый приложением, которое содержит элемент управления WebBrowser, если этот объект доступен.</span><span class="sxs-lookup"><span data-stu-id="3c400-111">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="3c400-112">В противном случае это свойство возвращает объект автоматизации элемента управления WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="3c400-112">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="3c400-113">Это свойство можно использовать с командами **Set** и **CreateObject** или с помощью команды **GetObject** для создания экземпляра приложения Windows Internet Explorer и управления им.</span><span class="sxs-lookup"><span data-stu-id="3c400-113">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c400-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3c400-114">Requirements</span></span>



| <span data-ttu-id="3c400-115">Требование</span><span class="sxs-lookup"><span data-stu-id="3c400-115">Requirement</span></span> | <span data-ttu-id="3c400-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3c400-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c400-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c400-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3c400-118">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3c400-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3c400-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c400-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3c400-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3c400-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3c400-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3c400-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c400-122"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c400-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="3c400-123">IDL</span><span class="sxs-lookup"><span data-stu-id="3c400-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3c400-124"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3c400-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="3c400-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3c400-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c400-126"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="3c400-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
