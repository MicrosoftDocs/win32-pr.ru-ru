---
title: дефаултикон
description: Содержит сведения о значке по умолчанию для однообъектных презентаций.
ms.assetid: 45a3289b-d9c4-4857-bf48-1fd664ce4430
keywords:
- COM раздела реестра Дефаултикон
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0079fb02f4429c1939f54d643e0a6b08fbc90eb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070675"
---
# <a name="defaulticon"></a><span data-ttu-id="98f9a-104">дефаултикон</span><span class="sxs-lookup"><span data-stu-id="98f9a-104">DefaultIcon</span></span>

<span data-ttu-id="98f9a-105">Содержит сведения о значке по умолчанию для однообъектных презентаций.</span><span class="sxs-lookup"><span data-stu-id="98f9a-105">Provides default icon information for iconic presentations of objects.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="98f9a-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="98f9a-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DefaultIcon = path, resourceID
```

## <a name="remarks"></a><span data-ttu-id="98f9a-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="98f9a-107">Remarks</span></span>

<span data-ttu-id="98f9a-108">Это значение **reg \_ SZ** , указывающее полный путь к исполняемому файлу приложения объекта и индексу ресурса значка в исполняемом файле.</span><span class="sxs-lookup"><span data-stu-id="98f9a-108">This is a **REG\_SZ** value that specifies the full path to the executable name of the object application and the resource index of the icon within the executable.</span></span>

<span data-ttu-id="98f9a-109">**Дефаултикон** определяет значок, используемый, если, например, элемент управления сведен к значку.</span><span class="sxs-lookup"><span data-stu-id="98f9a-109">**DefaultIcon** identifies the icon to use when, for example, a control is minimized to an icon.</span></span> <span data-ttu-id="98f9a-110">Эта запись содержит полный путь к исполняемому файлу серверного приложения и индексу ресурса значка в исполняемом файле.</span><span class="sxs-lookup"><span data-stu-id="98f9a-110">This entry contains the full path to the executable name of the server application and the resource index of the icon within the executable.</span></span> <span data-ttu-id="98f9a-111">Приложения могут использовать сведения, предоставляемые **дефаултикон** , для получения маркера значка с помощью [**екстрактикон**](/windows/win32/api/shellapi/nf-shellapi-extracticona).</span><span class="sxs-lookup"><span data-stu-id="98f9a-111">Applications can use the information provided by **DefaultIcon** to obtain an icon handle with [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona).</span></span>

 

 