---
description: Если для этой системной политики на уровне компьютера задано значение &\# 0034; 1&\# 0034;, установщик записывает в отладчик общие сообщения отладки с помощью функции OutputDebugString.
ms.assetid: 0a9416ca-0535-4595-a4f3-b3ef7c2d3a13
title: Отладка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2615b12bb76f4c4da0677bbeb459fa549f8233e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910980"
---
# <a name="debug"></a><span data-ttu-id="999a3-103">Отладка</span><span class="sxs-lookup"><span data-stu-id="999a3-103">Debug</span></span>

<span data-ttu-id="999a3-104">Если для этой [системной политики](system-policy.md) на уровне компьютера задано значение "1", установщик записывает в отладчик общие сообщения отладки с помощью функции [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) .</span><span class="sxs-lookup"><span data-stu-id="999a3-104">If this per-machine [system policy](system-policy.md) is set to "1", the installer writes common debugging messages to the debugger using the [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) function.</span></span> <span data-ttu-id="999a3-105">Если это значение равно 2, установщик записывает все допустимые сообщения отладки в отладчик с помощью функции [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) .</span><span class="sxs-lookup"><span data-stu-id="999a3-105">If this value is set to "2", the installer writes all valid debugging messages to the debugger using the [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) function.</span></span> <span data-ttu-id="999a3-106">Эта политика предназначена только для отладки и может не поддерживаться в будущих версиях установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="999a3-106">This policy is for debugging purposes only and may not be supported in future versions of Windows Installer.</span></span>

<span data-ttu-id="999a3-107">Установщик Windows только записывает командные строки в файл журнала, если в значении политики отладки задан третий бит (0x04).</span><span class="sxs-lookup"><span data-stu-id="999a3-107">Windows Installer only writes command lines into the log file if the third (0x04) bit is set in the value of the Debug policy.</span></span> <span data-ttu-id="999a3-108">Таким образом, чтобы отобразить командные строки в журнале, задайте для параметра политики отладки значение 7.</span><span class="sxs-lookup"><span data-stu-id="999a3-108">Therefore, to display command lines in the log, set the Debug policy value to 7.</span></span> <span data-ttu-id="999a3-109">При этом не отображаются свойства, связанные с [элементом управления](edit-control.md) "поле ввода", имеющим [атрибут элемента управления Password](password-control-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="999a3-109">This does not display properties associated with an [Edit Control](edit-control.md) having the [Password Control Attribute](password-control-attribute.md).</span></span> <span data-ttu-id="999a3-110">Это сделает свойства, заданные в командной строке, видимыми в журнале, даже если свойство включено в свойство [**мсихидденпропертиес**](msihiddenproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="999a3-110">This will make properties set on the command line visible in the log even if the property is included in the [**MsiHiddenProperties**](msihiddenproperties.md) property.</span></span> <span data-ttu-id="999a3-111">Дополнительные сведения см. в разделе [предотвращение записи конфиденциальной информации в файл журнала](preventing-confidential-information-from-being-written-into-the-log-file.md).</span><span class="sxs-lookup"><span data-stu-id="999a3-111">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="999a3-112">Ключ реестра</span><span class="sxs-lookup"><span data-stu-id="999a3-112">Registry Key</span></span>

<span data-ttu-id="999a3-113">**HKey \_ \_** \\ **Политики программного обеспечения** локального компьютера \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="999a3-113">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="999a3-114">Тип данных</span><span class="sxs-lookup"><span data-stu-id="999a3-114">Data Type</span></span>

<span data-ttu-id="999a3-115">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="999a3-115">**REG\_DWORD**</span></span>

 

 
