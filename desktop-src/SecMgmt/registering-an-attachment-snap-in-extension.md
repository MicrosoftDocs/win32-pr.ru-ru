---
description: После создания расширения оснастки вложения необходимо зарегистрировать его, чтобы оснастки MMC и настройки безопасности могли их искать и использовать.
ms.assetid: 176a658c-b1fd-40c5-a2ac-c9a2b7060c55
title: Регистрация расширения оснастки "вложение"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7726131325433aa920ff22c9b71a4f7184000a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682582"
---
# <a name="registering-an-attachment-snap-in-extension"></a><span data-ttu-id="e1197-103">Регистрация расширения оснастки "вложение"</span><span class="sxs-lookup"><span data-stu-id="e1197-103">Registering an Attachment Snap-in Extension</span></span>

<span data-ttu-id="e1197-104">После создания расширения оснастки вложения необходимо зарегистрировать его, чтобы оснастки MMC и настройки безопасности могли их искать и использовать.</span><span class="sxs-lookup"><span data-stu-id="e1197-104">After you create an attachment snap-in extension, you must register it in order for the MMC and the Security Configuration snap-ins to locate and use it.</span></span>

<span data-ttu-id="e1197-105">Оснастка "вложение" должна расширить пространство имен оснастки "Настройка безопасности", добавив собственный узел, как описано в следующей процедуре.</span><span class="sxs-lookup"><span data-stu-id="e1197-105">Your attachment snap-in must extend the Security Configuration snap-ins namespace by adding its own node as described in the following procedure.</span></span>

<span data-ttu-id="e1197-106">**Установка и регистрация расширения оснастки «вложение»**</span><span class="sxs-lookup"><span data-stu-id="e1197-106">**To install and register the attachment snap-in extension**</span></span>

1.  <span data-ttu-id="e1197-107">Зарегистрируйте расширение оснастки в следующем разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="e1197-107">Register the snap-in extension under the following registry key.</span></span> <span data-ttu-id="e1197-108">Не создавайте автономный ключ в оснастке. расширения оснасток вложения должны быть только расширениями.</span><span class="sxs-lookup"><span data-stu-id="e1197-108">Do not create a StandAlone key under the snap-in; attachment snap-ins extensions must only be extensions.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             MMC
                SnapIns
    ```

2.  <span data-ttu-id="e1197-109">Зарегистрируйте расширение оснастки вложений в следующих подразделах.</span><span class="sxs-lookup"><span data-stu-id="e1197-109">Register the attachment snap-in extension under the following subkeys.</span></span> <span data-ttu-id="e1197-110">Это можно сделать в рамках реализации функций **DllRegisterServer** и **DllUnregisterServer** .</span><span class="sxs-lookup"><span data-stu-id="e1197-110">This can be done as part of your **DllRegisterServer** and **DllUnregisterServer** function implementations.</span></span>

    <span data-ttu-id="e1197-111">Пространство имен [шаблонов безопасности](security-templates.md) :</span><span class="sxs-lookup"><span data-stu-id="e1197-111">[Security Templates](security-templates.md) namespace:</span></span>

    ```
    HKLM
       SOFTWARE
          Microsoft
             MMC
                NodeTypes
                   24a7f717-1f0c-11d1-affb-00c04fb984f9
                      Extensions
                         NameSpace
    ```

    <span data-ttu-id="e1197-112">Пространство имен [настройки и анализа безопасности](security-configuration-and-analysis.md) :</span><span class="sxs-lookup"><span data-stu-id="e1197-112">[Security Configuration and Analysis](security-configuration-and-analysis.md) namespace:</span></span>

    ```
    HKLM
       SOFTWARE
          Microsoft
             MMC
                NodeTypes
                   678050c7-1ff8-11d1-affb-00c04fb984f9
                      Extensions
                         NameSpace
    ```

 

 



