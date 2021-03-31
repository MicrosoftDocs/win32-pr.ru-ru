---
title: треатас
description: Указывает идентификатор CLSID класса, который может эмулировать текущий класс.
ms.assetid: 1d7a1677-738a-4258-9afc-e77bd0dcf40f
keywords:
- COM раздела реестра Треатас
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4340b398d6a98b0445cee932da120e23355b71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888635"
---
# <a name="treatas"></a><span data-ttu-id="4e7cc-104">треатас</span><span class="sxs-lookup"><span data-stu-id="4e7cc-104">TreatAs</span></span>

<span data-ttu-id="4e7cc-105">Указывает идентификатор CLSID класса, который может эмулировать текущий класс.</span><span class="sxs-lookup"><span data-stu-id="4e7cc-105">Specifies the CLSID of a class that can emulate the current class.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="4e7cc-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="4e7cc-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      TreatAs = {CLSID_TreatAs}
```

## <a name="remarks"></a><span data-ttu-id="4e7cc-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4e7cc-107">Remarks</span></span>

<span data-ttu-id="4e7cc-108">Это значение **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="4e7cc-108">This is a **REG\_SZ** value.</span></span>

<span data-ttu-id="4e7cc-109">Эмуляция — это способность одного приложения открывать и редактировать объект другого класса, сохраняя исходный формат объекта.</span><span class="sxs-lookup"><span data-stu-id="4e7cc-109">Emulation is the ability of one application to open and edit an object of a different class, while retaining the original format of the object.</span></span> <span data-ttu-id="4e7cc-110">Разрешение происходит на локальном компьютере, поэтому в случае удаленной активации разрешение происходит на клиентском компьютере с использованием идентификатора CLSID, заданного параметром **треатас**.</span><span class="sxs-lookup"><span data-stu-id="4e7cc-110">Resolution occurs on the local computer, so in remote activation case, resolution occurs on the client computer using the CLSID specified by **TreatAs**.</span></span>

<span data-ttu-id="4e7cc-111">DCOM просматривает локальный реестр для **треатас**, даже если вызвать функцию [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) и указать удаленный сервер.</span><span class="sxs-lookup"><span data-stu-id="4e7cc-111">DCOM looks at the local registry for **TreatAs**, even if you call the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function and specify a remote server.</span></span> <span data-ttu-id="4e7cc-112">Это означает, что если имеется запись **треатас** для класса Class1, которую следует рассматривать как Class2 на локальном компьютере, но вы вызываете **CoCreateInstance** для создания экземпляра Class1 и указываете удаленный сервер, DCOM попытается создать экземпляр класса Class2 на удаленном сервере, даже если Class2 не зарегистрирован на удаленном сервере, что приведет к сбою вызова **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="4e7cc-112">This means that if you have a **TreatAs** entry for Class1 to be treated as Class2 on your local computer, but you call **CoCreateInstance** to create an instance of Class1 and you specify a remote server, DCOM will try to create an instance of Class2 on the remote server, even if Class2 is not registered on the remote server, which will cause the call to **CoCreateInstance** to fail.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e7cc-113">См. также</span><span class="sxs-lookup"><span data-stu-id="4e7cc-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e7cc-114">**аутотреатас**</span><span class="sxs-lookup"><span data-stu-id="4e7cc-114">**AutoTreatAs**</span></span>](autotreatas.md)
</dt> <dt>

[<span data-ttu-id="4e7cc-115">**кожеттреатаскласс**</span><span class="sxs-lookup"><span data-stu-id="4e7cc-115">**CoGetTreatAsClass**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogettreatasclass)
</dt> <dt>

[<span data-ttu-id="4e7cc-116">**котреатаскласс**</span><span class="sxs-lookup"><span data-stu-id="4e7cc-116">**CoTreatAsClass**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cotreatasclass)
</dt> </dl>

 

 




