---
title: сервицепараметерс
description: Указывает параметры командной строки, передаваемые в объект, установленный для использования COM через значение реестра LocalService.
ms.assetid: da11e422-c0f2-4e44-9728-740ea6b61421
keywords:
- COM-значение реестра Сервицепараметерс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235de1052df72e88e2093647928ed68ab67451cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330163"
---
# <a name="serviceparameters"></a><span data-ttu-id="bfdcd-104">сервицепараметерс</span><span class="sxs-lookup"><span data-stu-id="bfdcd-104">ServiceParameters</span></span>

<span data-ttu-id="bfdcd-105">Указывает параметры командной строки, передаваемые в объект, установленный для использования COM через значение реестра [**LocalService**](localservice.md) .</span><span class="sxs-lookup"><span data-stu-id="bfdcd-105">Specifies the command-line parameters to be passed to an object installed for use by COM through the [**LocalService**](localservice.md) registry value.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="bfdcd-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="bfdcd-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ServiceParameters = parameter
```

## <a name="remarks"></a><span data-ttu-id="bfdcd-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bfdcd-107">Remarks</span></span>

<span data-ttu-id="bfdcd-108">Это значение **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="bfdcd-108">This is a **REG\_SZ** value.</span></span> <span data-ttu-id="bfdcd-109">Эта строка передается в службу в виде аргумента командной строки при запуске.</span><span class="sxs-lookup"><span data-stu-id="bfdcd-109">This string is passed to the service as a command-line argument as it is being launched.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfdcd-110">См. также</span><span class="sxs-lookup"><span data-stu-id="bfdcd-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfdcd-111">**локальная служба.**</span><span class="sxs-lookup"><span data-stu-id="bfdcd-111">**LocalService**</span></span>](localservice.md)
</dt> <dt>

[<span data-ttu-id="bfdcd-112">Регистрация серверов COM</span><span class="sxs-lookup"><span data-stu-id="bfdcd-112">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 




