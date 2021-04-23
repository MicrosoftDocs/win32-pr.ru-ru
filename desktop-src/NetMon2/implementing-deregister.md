---
description: Сетевой монитор передает все кадры записи в средства синтаксического анализа, а затем запускает вызов функции дерегистрации для всех определяемых им протоколов. Каждая библиотека DLL анализатора должна реализовывать функцию дерегистрации для каждого протокола, поддерживаемого библиотекой DLL средства синтаксического анализа.
ms.assetid: 936d5b00-b0ee-4a29-9396-1e2a7a91a2dd
title: Реализация отмены регистрации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee07c5b6b3c746e9c29811332b9e7674e49db26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650517"
---
# <a name="implementing-deregister"></a><span data-ttu-id="7c99e-104">Реализация отмены регистрации</span><span class="sxs-lookup"><span data-stu-id="7c99e-104">Implementing Deregister</span></span>

<span data-ttu-id="7c99e-105">Сетевой монитор передает все кадры записи в средства синтаксического анализа, а затем запускает вызов функции [**дерегистрации**](deregister.md) для всех определяемых им протоколов.</span><span class="sxs-lookup"><span data-stu-id="7c99e-105">Network Monitor passes all the frames of a capture to the parsers, and then starts calling the [**Deregister**](deregister.md) function for all the protocols it identifies.</span></span> <span data-ttu-id="7c99e-106">Каждая библиотека DLL анализатора должна реализовывать функцию **дерегистрации** для каждого протокола, ПОДДЕРЖИВАЕМого библиотекой DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="7c99e-106">Each parser DLL must implement a **Deregister** function for each protocol that the parser DLL supports.</span></span>

<span data-ttu-id="7c99e-107">Каждая реализация функции [**дерегистрации**](deregister.md) должна вызывать функцию [**дестройпротоколдатабасе**](destroypropertydatabase.md) для освобождения ресурсов, используемых для создания базы данных.</span><span class="sxs-lookup"><span data-stu-id="7c99e-107">Each implementation of the [**Deregister**](deregister.md) function must call the [**DestroyProtocolDatabase**](destroypropertydatabase.md) function to release the resources that are used to create the database.</span></span>

<span data-ttu-id="7c99e-108">Следующая процедура определяет один шаг, необходимый для реализации [**отмены регистрации**](deregister.md).</span><span class="sxs-lookup"><span data-stu-id="7c99e-108">The following procedure identifies the one step necessary to implement [**Deregister**](deregister.md).</span></span>

<span data-ttu-id="7c99e-109">**Реализация отмены регистрации для одного протокола**</span><span class="sxs-lookup"><span data-stu-id="7c99e-109">**To implement Deregister for one protocol**</span></span>

-   <span data-ttu-id="7c99e-110">Вызовите [**дестройпротоколдатабасе**](destroypropertydatabase.md) , чтобы освободить ресурсы базы данных.</span><span class="sxs-lookup"><span data-stu-id="7c99e-110">Call [**DestroyProtocolDatabase**](destroypropertydatabase.md) to release the database resources.</span></span>

<span data-ttu-id="7c99e-111">Ниже приведена базовая реализация [**отмены регистрации**](deregister.md).</span><span class="sxs-lookup"><span data-stu-id="7c99e-111">The following is a basic implementation of [**Deregister**](deregister.md).</span></span> <span data-ttu-id="7c99e-112">Обратите внимание, что в примере кода показан выпуск ресурсов, которые используются для создания базы данных свойств.</span><span class="sxs-lookup"><span data-stu-id="7c99e-112">Note that the code example shows the release of resources that are used to create a property database.</span></span>

``` syntax
#include <windows.h>

VOID WINAPI MyProtocolDeregister (HPROTOCOL hProtocol)
{
  DestroyPropertyDatabase (hProtocol);
}
```

 

 



