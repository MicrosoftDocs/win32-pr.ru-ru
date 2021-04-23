---
description: Содержит объект приложения папки.
ms.assetid: 1dba83eb-1af6-42d9-b2c9-ab7767888efe
title: Свойство Folder. Application (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Application
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: 13a6a90dd324498c332f7bf580ff5ec987a0c5b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496782"
---
# <a name="folderapplication-property"></a><span data-ttu-id="15909-103">Свойство Folder. Application</span><span class="sxs-lookup"><span data-stu-id="15909-103">Folder.Application property</span></span>

<span data-ttu-id="15909-104">Содержит объект приложения папки.</span><span class="sxs-lookup"><span data-stu-id="15909-104">Contains the folder's Application object.</span></span>

<span data-ttu-id="15909-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="15909-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="15909-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15909-106">Syntax</span></span>


```JScript
Application = Folder.Application
```



## <a name="property-value"></a><span data-ttu-id="15909-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="15909-107">Property value</span></span>

<span data-ttu-id="15909-108">Ссылка на объект приложения.</span><span class="sxs-lookup"><span data-stu-id="15909-108">An object reference to the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="15909-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="15909-109">Remarks</span></span>

<span data-ttu-id="15909-110">Свойство **Application** возвращает объект автоматизации, поддерживаемый приложением, которое содержит элемент управления WebBrowser, если этот объект доступен.</span><span class="sxs-lookup"><span data-stu-id="15909-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="15909-111">В противном случае это свойство возвращает объект автоматизации элемента управления WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="15909-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="15909-112">Это свойство можно использовать с командами **Set** и **CreateObject** или с помощью команды **GetObject** для создания экземпляра приложения Internet Explorer и управления им.</span><span class="sxs-lookup"><span data-stu-id="15909-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Internet Explorer application.</span></span>

> [!Note]  
> <span data-ttu-id="15909-113">Не все методы реализуются для всех папок.</span><span class="sxs-lookup"><span data-stu-id="15909-113">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="15909-114">Например, метод [**PARSENAME**](folder-parsename.md) не реализован для папки панели управления ( \_ элементы управления CSID).</span><span class="sxs-lookup"><span data-stu-id="15909-114">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="15909-115">При попытке вызвать нереализованный метод возникнет ошибка 0x800A01BD (Decimal 445).</span><span class="sxs-lookup"><span data-stu-id="15909-115">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="15909-116">Требования</span><span class="sxs-lookup"><span data-stu-id="15909-116">Requirements</span></span>



| <span data-ttu-id="15909-117">Требование</span><span class="sxs-lookup"><span data-stu-id="15909-117">Requirement</span></span> | <span data-ttu-id="15909-118">Значение</span><span class="sxs-lookup"><span data-stu-id="15909-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="15909-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15909-119">Minimum supported client</span></span><br/> | <span data-ttu-id="15909-120">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="15909-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                 |
| <span data-ttu-id="15909-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15909-121">Minimum supported server</span></span><br/> | <span data-ttu-id="15909-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="15909-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="15909-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="15909-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="15909-124"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="15909-124"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="15909-125">IDL</span><span class="sxs-lookup"><span data-stu-id="15909-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="15909-126"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="15909-126"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




