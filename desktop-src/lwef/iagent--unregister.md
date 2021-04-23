---
title: Отмена регистрации Иажент
description: Отмена регистрации Иажент
ms.assetid: d81cde72-f9ff-45aa-9dbf-faea9a478c3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796e033ac823ee7c79fe5312fab2c57dec36e694
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890632"
---
# <a name="iagentunregister"></a><span data-ttu-id="0d87e-103">Иажент:: Отмена регистрации</span><span class="sxs-lookup"><span data-stu-id="0d87e-103">IAgent::Unregister</span></span>

<span data-ttu-id="0d87e-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0d87e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Unregister(
   long dwSinkID  //notification sink ID
);
```

<span data-ttu-id="0d87e-105">Выгружает символьные данные для указанного символа из коллекции [**символов**](/windows/desktop/lwef/the-characters-object) .</span><span class="sxs-lookup"><span data-stu-id="0d87e-105">Unloads the character data for the specified character from the [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span>

-   <span data-ttu-id="0d87e-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="0d87e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0d87e-107"><span id="dwSinkID"></span><span id="dwsinkid"></span><span id="DWSINKID"></span>*двсинкид*</span><span class="sxs-lookup"><span data-stu-id="0d87e-107"><span id="dwSinkID"></span><span id="dwsinkid"></span><span id="DWSINKID"></span>*dwSinkID*</span></span>
</dt> <dd>

<span data-ttu-id="0d87e-108">ИДЕНТИФИКАТОР приемника уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0d87e-108">The notification sink ID.</span></span>

</dd> </dl>

<span data-ttu-id="0d87e-109">Используйте этот метод, если вам больше не нужны службы агента Майкрософт, например при завершении работы приложения.</span><span class="sxs-lookup"><span data-stu-id="0d87e-109">Use this method when you no longer need Microsoft Agent services, such as when your application shuts down.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d87e-110">См. также:</span><span class="sxs-lookup"><span data-stu-id="0d87e-110">See Also</span></span>

[<span data-ttu-id="0d87e-111">**Иажент:: Register**</span><span class="sxs-lookup"><span data-stu-id="0d87e-111">**IAgent::Register**</span></span>](iagent--register.md)


 

 