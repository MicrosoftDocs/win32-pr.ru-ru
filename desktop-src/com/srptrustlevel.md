---
title: срптрустлевел
description: Задает уровень доверия политики ограниченного использования программ (SRP) для приложений.
ms.assetid: 2ec10eb5-f83a-4ce7-8e03-36cdafadf169
keywords:
- COM-значение реестра Срптрустлевел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c1e9290cbe04cfe33e1192b95b86ca03fd5ea5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410787"
---
# <a name="srptrustlevel"></a><span data-ttu-id="47af1-104">срптрустлевел</span><span class="sxs-lookup"><span data-stu-id="47af1-104">SRPTrustLevel</span></span>

<span data-ttu-id="47af1-105">Задает уровень доверия политики ограниченного использования программ (SRP) для приложений.</span><span class="sxs-lookup"><span data-stu-id="47af1-105">Sets the software restriction policy (SRP) trust level for applications.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="47af1-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="47af1-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      SRPTrustLevel = value
```

## <a name="remarks"></a><span data-ttu-id="47af1-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="47af1-107">Remarks</span></span>

<span data-ttu-id="47af1-108">Это значение **reg \_ DWORD** , которое доступно в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="47af1-108">This is a **REG\_DWORD** value that is available starting with Windows XP.</span></span>



| <span data-ttu-id="47af1-109">Значение</span><span class="sxs-lookup"><span data-stu-id="47af1-109">Value</span></span>                                 | <span data-ttu-id="47af1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="47af1-110">Description</span></span>                                                                          |
|---------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="47af1-111">0x0 (более безопасные \_ LEVELID \_ запрещены)</span><span class="sxs-lookup"><span data-stu-id="47af1-111">0x0 (SAFER\_LEVELID\_DISALLOWED)</span></span>      | <span data-ttu-id="47af1-112">Приложение не может получить доступ к привилегиям пользователей и с учетом параметров безопасности.</span><span class="sxs-lookup"><span data-stu-id="47af1-112">The application is disallowed from accessing and security-sensitive user privileges.</span></span> |
| <span data-ttu-id="47af1-113">0x40000 (безопасность \_ LEVELID \_ фуллитрустед)</span><span class="sxs-lookup"><span data-stu-id="47af1-113">0x40000 (SAFE\_LEVELID\_FULLYTRUSTED)</span></span> | <span data-ttu-id="47af1-114">Приложение имеет неограниченный доступ к привилегиям пользователя.</span><span class="sxs-lookup"><span data-stu-id="47af1-114">The application has unrestricted access to the user's privileges.</span></span>                    |



 

<span data-ttu-id="47af1-115">Если значение **срптрустлевел** не существует, используется значение по умолчанию, равное более безопасному \_ LEVELID \_ запрещенному.</span><span class="sxs-lookup"><span data-stu-id="47af1-115">If the **SRPTrustLevel** value does not exist, the default value of SAFER\_LEVELID\_DISALLOWED is used.</span></span> <span data-ttu-id="47af1-116">Если **срптрустлевел** имеет неправильный тип или выходит за пределы допустимого диапазона, com ВОЗВРАЩАЕТ ошибку комадмин \_ E \_ саферинвалид.</span><span class="sxs-lookup"><span data-stu-id="47af1-116">If **SRPTrustLevel** is of the wrong type or out of range, COM returns the error COMADMIN\_E\_SAFERINVALID.</span></span> <span data-ttu-id="47af1-117">Если активация любой сортировки завершается неудачей из-за проверок доверия SRP, COM возвращает ошибку CO \_ E \_ активатионфаилед.</span><span class="sxs-lookup"><span data-stu-id="47af1-117">If an activation of any sort fails because of SRP trust checks, COM returns the error CO\_E\_ACTIVATIONFAILED.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47af1-118">См. также</span><span class="sxs-lookup"><span data-stu-id="47af1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47af1-119">Безопасность в COM</span><span class="sxs-lookup"><span data-stu-id="47af1-119">Security in COM</span></span>](security-in-com.md)
</dt> <dt>

[<span data-ttu-id="47af1-120">**српактиватеасактиваторчеккс**</span><span class="sxs-lookup"><span data-stu-id="47af1-120">**SRPActivateAsActivatorChecks**</span></span>](srpactivateasactivatorchecks.md)
</dt> <dt>

[<span data-ttu-id="47af1-121">**српруннингобжектчеккс**</span><span class="sxs-lookup"><span data-stu-id="47af1-121">**SRPRunningObjectChecks**</span></span>](srprunningobjectchecks.md)
</dt> </dl>

 

 




