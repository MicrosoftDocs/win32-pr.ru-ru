---
title: лоадусерсеттингс
description: Определяет, будет ли COM загружать профиль пользователя для COM-серверов, запущенных в качестве запускающего удостоверения пользовательского приложения.
ms.assetid: 3e2b3249-3747-4d98-96da-f3e480a51d12
keywords:
- COM-значение реестра Лоадусерсеттингс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e14282b00bc2c2d9b989e19480047f115623d55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986672"
---
# <a name="loadusersettings"></a><span data-ttu-id="029bd-104">лоадусерсеттингс</span><span class="sxs-lookup"><span data-stu-id="029bd-104">LoadUserSettings</span></span>

<span data-ttu-id="029bd-105">Определяет, будет ли COM загружать профиль пользователя для COM-серверов, запущенных в качестве запускающего удостоверения пользовательского приложения.</span><span class="sxs-lookup"><span data-stu-id="029bd-105">Determines whether COM will load the user profile for COM servers running as the launching user application identity.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="029bd-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="029bd-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LoadUserSettings = value
```

## <a name="remarks"></a><span data-ttu-id="029bd-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="029bd-107">Remarks</span></span>

<span data-ttu-id="029bd-108">Это значение **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="029bd-108">This is a **REG\_DWORD** value.</span></span> <span data-ttu-id="029bd-109">Если *значение* не равно нулю, com загружает профиль учетной записи пользователя, с помощью которой он запускает COM-сервер.</span><span class="sxs-lookup"><span data-stu-id="029bd-109">If *value* is nonzero, COM loads the profile of the user account with which it launches the COM server.</span></span> <span data-ttu-id="029bd-110">Если *значение* равно нулю или отсутствует, com не будет загружать профиль учетной записи пользователя, с помощью которой он запускает COM-сервер.</span><span class="sxs-lookup"><span data-stu-id="029bd-110">If *value* is zero or not present, COM will not load the profile of the user account with which it launches the COM server.</span></span>

<span data-ttu-id="029bd-111">Этот параметр игнорируется, если имеется запись [**запуска от имени**](runas.md) .</span><span class="sxs-lookup"><span data-stu-id="029bd-111">This setting is ignored if a [**RunAs**](runas.md) entry is present.</span></span>

 

 




