---
title: ротфлагс
description: Управляет регистрацией сервера COM в работающей таблице объектов (ROT).
ms.assetid: a27c04e5-b1d3-4cb5-9b2c-9ae45663cf56
keywords:
- COM-значение реестра Ротфлагс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d52bc0c07ee6c86015ad1b997f2f21e33dda9a1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700523"
---
# <a name="rotflags"></a><span data-ttu-id="37611-104">ротфлагс</span><span class="sxs-lookup"><span data-stu-id="37611-104">ROTFlags</span></span>

<span data-ttu-id="37611-105">Управляет регистрацией сервера COM в работающей таблице объектов (ROT).</span><span class="sxs-lookup"><span data-stu-id="37611-105">Controls the registration of a COM server in the running object table (ROT).</span></span>

## <a name="registry-entry"></a><span data-ttu-id="37611-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="37611-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ROTFlags = flags
```

## <a name="remarks"></a><span data-ttu-id="37611-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="37611-107">Remarks</span></span>

<span data-ttu-id="37611-108">Это значение **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="37611-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="37611-109">Значение флага</span><span class="sxs-lookup"><span data-stu-id="37611-109">Flag Value</span></span> | <span data-ttu-id="37611-110">Константа</span><span class="sxs-lookup"><span data-stu-id="37611-110">Constant</span></span>                        |
|------------|---------------------------------|
| <span data-ttu-id="37611-111">0x1</span><span class="sxs-lookup"><span data-stu-id="37611-111">0x1</span></span>        | <span data-ttu-id="37611-112">**РОТРЕГФЛАГС \_ аллованиклиент**</span><span class="sxs-lookup"><span data-stu-id="37611-112">**ROTREGFLAGS\_ALLOWANYCLIENT**</span></span> |



 

### <a name="rotregflags_allowanyclient-description"></a><span data-ttu-id="37611-113">\_Описание ротрегфлагс аллованиклиент</span><span class="sxs-lookup"><span data-stu-id="37611-113">ROTREGFLAGS\_ALLOWANYCLIENT Description</span></span>

<span data-ttu-id="37611-114">Если сервер COM хочет зарегистрировать в таблице ROT и разрешить любому клиенту доступ к регистрации, он должен использовать флаг **ротфлагс \_ аллованиклиент** .</span><span class="sxs-lookup"><span data-stu-id="37611-114">If a COM server wants to register in the ROT and allow any client to access the registration, it must use the **ROTFLAGS\_ALLOWANYCLIENT** flag.</span></span> <span data-ttu-id="37611-115">Сервер COM "активировать как активатор" не может указать **ротфлагс \_ аллованиклиент** , так как диспетчер управления СЛУЖБАМИ DCOM (дкомскм) принудительно проверяет подделку по этому флагу.</span><span class="sxs-lookup"><span data-stu-id="37611-115">An "Activate As Activator" COM server cannot specify **ROTFLAGS\_ALLOWANYCLIENT** because the DCOM service control manager (DCOMSCM) enforces a spoof check against this flag.</span></span> <span data-ttu-id="37611-116">Таким образом, в Windows Vista и более поздних версиях COM добавляет поддержку записи реестра **ротфлагс** , которая позволяет серверу указать, что его регистрации в таблице ROT будут доступны любому клиенту.</span><span class="sxs-lookup"><span data-stu-id="37611-116">Therefore, in Windows Vista and later, COM adds support for the **ROTFlags** registry entry that allows the server to stipulate that its ROT registrations be made available to any client.</span></span>

<span data-ttu-id="37611-117">Запись должна существовать в кусте **" \_ локальный \_ компьютер" hKey** .</span><span class="sxs-lookup"><span data-stu-id="37611-117">The entry must exist in the **HKEY\_LOCAL\_MACHINE** hive.</span></span> <span data-ttu-id="37611-118">Эта запись предоставляет сервер "Активация в качестве активатора" с теми же функциональными возможностями, которые **ротфлагс \_ аллованиклиент** предоставляет для сервера запуска от имени.</span><span class="sxs-lookup"><span data-stu-id="37611-118">This entry provides an "Activate As Activator" server with the same functionality that **ROTFLAGS\_ALLOWANYCLIENT** provides for a RunAs server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37611-119">См. также</span><span class="sxs-lookup"><span data-stu-id="37611-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37611-120">Ключ AppID</span><span class="sxs-lookup"><span data-stu-id="37611-120">AppID Key</span></span>](appid-key.md)
</dt> <dt>

[<span data-ttu-id="37611-121">Регистрация серверов COM</span><span class="sxs-lookup"><span data-stu-id="37611-121">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="37611-122">Безопасность в COM</span><span class="sxs-lookup"><span data-stu-id="37611-122">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




