---
title: активатеатстораже
description: Настраивает Клиент для создания экземпляров объектов на том же компьютере, что и сохраняемое состояние, которое они используют или откуда инициализируются.
ms.assetid: bc0f0c1c-dbfc-4b7a-b897-3646afe3f6bb
keywords:
- значение реестра COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2ddd1330191d7b7baf37973dbfb40e267a2f87e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070710"
---
# <a name="activateatstorage"></a><span data-ttu-id="4428f-104">активатеатстораже</span><span class="sxs-lookup"><span data-stu-id="4428f-104">ActivateAtStorage</span></span>

<span data-ttu-id="4428f-105">Настраивает Клиент для создания экземпляров объектов на том же компьютере, что и сохраняемое состояние, которое они используют или откуда инициализируются.</span><span class="sxs-lookup"><span data-stu-id="4428f-105">Configures the client to instantiate objects on the same computer as the persistent state they are using or from which they are initialized.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="4428f-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="4428f-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ActivateAtStorage = value
```

## <a name="remarks"></a><span data-ttu-id="4428f-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4428f-107">Remarks</span></span>

<span data-ttu-id="4428f-108">Это значение **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="4428f-108">This is a **REG\_SZ** value.</span></span> <span data-ttu-id="4428f-109">Любое значение, которое начинается с "Y" или "y", указывает, что следует использовать **активатеатстораже** .</span><span class="sxs-lookup"><span data-stu-id="4428f-109">Any value that begins with 'Y' or 'y' indicates that **ActivateAtStorage** should be used.</span></span>

<span data-ttu-id="4428f-110">Функция **активатеатстораже** обеспечивает прозрачный способ, позволяющий клиентам размещать выполняющиеся объекты на том же компьютере, где находятся используемые ими данные.</span><span class="sxs-lookup"><span data-stu-id="4428f-110">The **ActivateAtStorage** capability provides a transparent way to allow clients to locate running objects on the same computer as the data that they use.</span></span> <span data-ttu-id="4428f-111">Это сокращает сетевой трафик, так как объект выполняет локальные вызовы файловой системы вместо вызовов по сети.</span><span class="sxs-lookup"><span data-stu-id="4428f-111">This reduces network traffic because the object performs local file-system calls instead of calls across the network.</span></span>

<span data-ttu-id="4428f-112">Если для **активатеатстораже** задано значение, оно становится поведением по умолчанию в вызовах функций [**кожетинстанцефромфиле**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) и [**кожетинстанцефромистораже**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) , а также в реализации моникера файла [**IMoniker:: биндтубжект**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).</span><span class="sxs-lookup"><span data-stu-id="4428f-112">When a value is set for **ActivateAtStorage**, this becomes the default behavior in calls to the [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) and [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) functions, as well as to the file moniker implementation of [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).</span></span> <span data-ttu-id="4428f-113">Во всех этих вызовах указание структуры [**косерверинфо**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) переопределяет значение параметра **активатеатстораже** на время вызова функции.</span><span class="sxs-lookup"><span data-stu-id="4428f-113">In all of these calls, specifying a [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure overrides the setting of **ActivateAtStorage** for the duration of the function call.</span></span> <span data-ttu-id="4428f-114">Вызывающий объект может передавать сведения о **косерверинфо** в **IMoniker:: Биндтубжект** через структуру [**привязки \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1) .</span><span class="sxs-lookup"><span data-stu-id="4428f-114">The caller can pass **COSERVERINFO** information to **IMoniker::BindToObject** through the [**BIND\_OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1) structure.</span></span>

<span data-ttu-id="4428f-115">Значение, заданное для **активатеатстораже** , также является поведением по умолчанию при \_ указании параметра клскткс Remote Server, \_ Если на клиентском компьютере не установлены данные реестра для класса.</span><span class="sxs-lookup"><span data-stu-id="4428f-115">The value set for **ActivateAtStorage** is also the default behavior when CLSCTX\_REMOTE\_SERVER is specified if no registry information for the class is installed on the client's computer.</span></span> <span data-ttu-id="4428f-116">Таким образом, клиентские приложения, написанные для использования преимуществ **активатеатстораже** , могут требовать меньше администрирования.</span><span class="sxs-lookup"><span data-stu-id="4428f-116">Client applications written to take advantage of **ActivateAtStorage** may therefore require less administration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4428f-117">См. также</span><span class="sxs-lookup"><span data-stu-id="4428f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4428f-118">**клскткс**</span><span class="sxs-lookup"><span data-stu-id="4428f-118">**CLSCTX**</span></span>](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> <dt>

[<span data-ttu-id="4428f-119">**кожетинстанцефромфиле**</span><span class="sxs-lookup"><span data-stu-id="4428f-119">**CoGetInstanceFromFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
</dt> <dt>

[<span data-ttu-id="4428f-120">**кожетинстанцефромистораже**</span><span class="sxs-lookup"><span data-stu-id="4428f-120">**CoGetInstanceFromIStorage**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
</dt> <dt>

[<span data-ttu-id="4428f-121">**косерверинфо**</span><span class="sxs-lookup"><span data-stu-id="4428f-121">**COSERVERINFO**</span></span>](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo)
</dt> <dt>

[<span data-ttu-id="4428f-122">**IMoniker:: Биндтубжект**</span><span class="sxs-lookup"><span data-stu-id="4428f-122">**IMoniker::BindToObject**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)
</dt> <dt>

[<span data-ttu-id="4428f-123">Регистрация серверов COM</span><span class="sxs-lookup"><span data-stu-id="4428f-123">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 