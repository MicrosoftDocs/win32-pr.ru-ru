---
description: Класс связи/Dataport/портнаме устройства состоит из имен устройств, к которым подключены модемы.
ms.assetid: 174519f6-3e73-4f05-9718-9e38680a0fb7
title: канал связи, модемы и портнаме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f926dc87a093f49d41256b003e47c048caa5ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911539"
---
# <a name="commdatamodemportname"></a><span data-ttu-id="9ec8c-103">канал связи, модемы и портнаме</span><span class="sxs-lookup"><span data-stu-id="9ec8c-103">comm/datamodem/portname</span></span>

<span data-ttu-id="9ec8c-104">Класс связи/Dataport/портнаме устройства состоит из имен устройств, к которым подключены модемы.</span><span class="sxs-lookup"><span data-stu-id="9ec8c-104">The comm/datamodem/portname device class consists of the device names to which modems are attached.</span></span> <span data-ttu-id="9ec8c-105">Если это имя устройства указано при вызове функции [**линежетид**](/windows/desktop/api/Tapi/nf-tapi-linegetid) , функция заполняет структуру [**ВАРСТРИНГ**](/windows/desktop/api/Tapi/ns-tapi-varstring) строкой ANSI (не Юникод), заканчивающейся нулем, с указанием имени порта, к которому подключен указанный модем, например COM1 \\ 0.</span><span class="sxs-lookup"><span data-stu-id="9ec8c-105">When this device name is specified in a call to the [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function, the function fills the [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure with a null-terminated ANSI (not Unicode) string specifying the name of the port to which the specified modem is attached, such as "COM1\\0".</span></span> <span data-ttu-id="9ec8c-106">Это предназначено в первую очередь для идентификации в пользовательском интерфейсе, но может использоваться в некоторых обстоятельствах для непосредственного открытия устройства, минуя поставщика услуг (если у поставщика услуг еще нет открытого устройства).</span><span class="sxs-lookup"><span data-stu-id="9ec8c-106">This is intended primarily for identification purposes in the user interface, but could be used under some circumstances to open the device directly, bypassing the service provider (if the service provider does not already have the device open itself).</span></span> <span data-ttu-id="9ec8c-107">Если с устройством не связан ни один порт, в структуре Варстринг возвращается пустая строка (" \\ 0") (  со строкой длиной 1).</span><span class="sxs-lookup"><span data-stu-id="9ec8c-107">If there is no port associated with the device, a null string ("\\0") is returned in the **VARSTRING** structure (with a string length of 1).</span></span>

 

 



