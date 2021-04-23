---
title: инвалидсекуритидескрипторлоггинглевел
description: Задает уровень детализации записей журнала событий о недопустимых дескрипторах безопасности для запуска компонента и разрешений на доступ.
ms.assetid: 44f680b8-083d-44f0-a353-e66b87787ab7
keywords:
- COM-значение реестра Инвалидсекуритидескрипторлоггинглевел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ac333a7cb8b54f383f93a71131cbb0a9314466
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328280"
---
# <a name="invalidsecuritydescriptorlogginglevel"></a><span data-ttu-id="a5d38-104">инвалидсекуритидескрипторлоггинглевел</span><span class="sxs-lookup"><span data-stu-id="a5d38-104">InvalidSecurityDescriptorLoggingLevel</span></span>

<span data-ttu-id="a5d38-105">Задает уровень детализации записей журнала событий о недопустимых дескрипторах безопасности для запуска компонента и разрешений на доступ.</span><span class="sxs-lookup"><span data-stu-id="a5d38-105">Sets the verbosity of event log entries about invalid security descriptors for component launch and access permissions.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="a5d38-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="a5d38-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   InvalidSecurityDescriptorLoggingLevel = value
```

## <a name="remarks"></a><span data-ttu-id="a5d38-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5d38-107">Remarks</span></span>

<span data-ttu-id="a5d38-108">Это значение **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="a5d38-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="a5d38-109">Значение</span><span class="sxs-lookup"><span data-stu-id="a5d38-109">Value</span></span> | <span data-ttu-id="a5d38-110">Описание</span><span class="sxs-lookup"><span data-stu-id="a5d38-110">Description</span></span>                                                                                                                                                                    |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5d38-111">1</span><span class="sxs-lookup"><span data-stu-id="a5d38-111">1</span></span>     | <span data-ttu-id="a5d38-112">Всегда заносить в журнал ошибки, когда COM находит недопустимый дескриптор безопасности.</span><span class="sxs-lookup"><span data-stu-id="a5d38-112">Always log failures when COM finds an invalid security descriptor.</span></span> <span data-ttu-id="a5d38-113">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a5d38-113">This is the default value.</span></span>                                                                                  |
| <span data-ttu-id="a5d38-114">2</span><span class="sxs-lookup"><span data-stu-id="a5d38-114">2</span></span>     | <span data-ttu-id="a5d38-115">Никогда не регистрировать ошибки, когда COM находит недопустимый дескриптор безопасности.</span><span class="sxs-lookup"><span data-stu-id="a5d38-115">Never log failures when COM finds an invalid security descriptor.</span></span> <span data-ttu-id="a5d38-116">Не рекомендуется отключать ведение журнала событий, так как это может усложнить диагностику проблем.</span><span class="sxs-lookup"><span data-stu-id="a5d38-116">It is not recommended that you disable event logging, as it can make it more difficult to diagnose problems.</span></span> |



 

<span data-ttu-id="a5d38-117">Если вы устанавливаете дескрипторы безопасности разрешений на запуск и доступ (обычно называемые ACL), можно создать описатель безопасности, значение которого не может быть интерпретировано неоднозначно.</span><span class="sxs-lookup"><span data-stu-id="a5d38-117">If you set launch and access permission security descriptors (commonly called ACLs) directly, it is possible to construct a security descriptor whose meaning cannot be interpreted unambiguously.</span></span> <span data-ttu-id="a5d38-118">COM создает запись в журнале событий при обнаружении такого недопустимого дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="a5d38-118">COM makes an event log entry when it encounters such an invalid security descriptor.</span></span>

<span data-ttu-id="a5d38-119">Обратите внимание, что [**активатионфаилурелоггинглевел**](activationfailurelogginglevel.md) и [**каллфаилурелоггинглевел**](callfailurelogginglevel.md) не имеют возможности контролировать ведение журнала недопустимых ошибок дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="a5d38-119">Note that [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md) and [**CallFailureLoggingLevel**](callfailurelogginglevel.md) have no control over logging invalid security descriptor errors.</span></span> <span data-ttu-id="a5d38-120">Используйте **инвалидсекуритидескрипторлоггинглевел** для полного контроля над этими функциями.</span><span class="sxs-lookup"><span data-stu-id="a5d38-120">Use **InvalidSecurityDescriptorLoggingLevel** for full control over this functionality.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5d38-121">См. также</span><span class="sxs-lookup"><span data-stu-id="a5d38-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5d38-122">Настройка безопасности для приложений COM</span><span class="sxs-lookup"><span data-stu-id="a5d38-122">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




