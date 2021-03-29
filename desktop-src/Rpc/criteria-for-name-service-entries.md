---
title: Критерии для записей службы имен
description: Критерий для записей службы имен с удаленным вызовом процедур (RPC).
ms.assetid: f9a7b935-7104-489c-93a8-0c3793d17348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb32314dc86b179ea98bdf07000dc5ea359bdc77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486889"
---
# <a name="criteria-for-name-service-entries"></a><span data-ttu-id="2c747-103">Критерии для записей службы имен</span><span class="sxs-lookup"><span data-stu-id="2c747-103">Criteria for Name Service Entries</span></span>

<span data-ttu-id="2c747-104">При обработке записей службы имен используются следующие критерии.</span><span class="sxs-lookup"><span data-stu-id="2c747-104">The following criteria are used when processing name service entries:</span></span>

-   <span data-ttu-id="2c747-105">Если указать имя записи, отличное от **null** , для [**рпкнсбиндинглукупбегин**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina), то эта запись будет единственной записью для поиска дескрипторов привязки.</span><span class="sxs-lookup"><span data-stu-id="2c747-105">If you provide a non-**NULL** entry name for [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina), that entry will be the only entry searched for binding handles.</span></span> <span data-ttu-id="2c747-106">Если передать **значение NULL**, будет выполнен поиск всех записей в домене входа в систему.</span><span class="sxs-lookup"><span data-stu-id="2c747-106">If you pass **NULL**, all entries in your logon domain will be searched.</span></span> <span data-ttu-id="2c747-107">Обратите внимание, что сюда не входят доверенные домены.</span><span class="sxs-lookup"><span data-stu-id="2c747-107">Note that this does not include trusted domains.</span></span>
-   <span data-ttu-id="2c747-108">Если вы предоставляете дескриптор интерфейса, дескрипторы привязки возвращаются из записи, только если раздел интерфейса записи содержит совместимую версию этого интерфейса UUID.</span><span class="sxs-lookup"><span data-stu-id="2c747-108">If you provide an interface handle, binding handles are returned from an entry only if the interface section of the entry contains a compatible version of that interface UUID.</span></span> <span data-ttu-id="2c747-109">То есть основной номер версии должен совпадать с идентификатором UUID интерфейса, а номер вспомогательной версии должен быть больше или равен вашему.</span><span class="sxs-lookup"><span data-stu-id="2c747-109">That is, the major version number must be the same as your interface UUID, while the minor version number must be equal to or greater than yours.</span></span>
-   <span data-ttu-id="2c747-110">Если указать UUID объекта, дескрипторы привязки возвращаются из записи только в том случае, если раздел UUID объекта содержит этот конкретный идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="2c747-110">If you provide an object UUID, binding handles are returned from an entry only if the object UUID section of the entry contains that particular object UUID.</span></span>

<span data-ttu-id="2c747-111">Если запись службы имен не сохранила описанные выше условия, собираются все дескрипторы привязки из этих записей.</span><span class="sxs-lookup"><span data-stu-id="2c747-111">If a name service entry survives the criteria described above, all the binding handles from those entries are gathered.</span></span> <span data-ttu-id="2c747-112">Дескрипторы с последовательностью протокола, не поддерживаемой клиентом, отбрасываются, и остальные дескрипторы возвращаются в качестве выходных данных [**рпкнсбиндинглукупнекст**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext).</span><span class="sxs-lookup"><span data-stu-id="2c747-112">Handles with a protocol sequence that is unsupported by the client are discarded and the remaining handles are returned to you as the output from [**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext).</span></span>

 

 




