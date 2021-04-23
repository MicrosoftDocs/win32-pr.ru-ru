---
description: Эта политика системы для компьютера используется, только если ведение журнала не включено с помощью \# параметра командной строки &0034;/l&\# 0034; или мсиенаблелог.
ms.assetid: d8649808-5dc3-4496-8c2f-da9b1512b5aa
title: Ведение журнала (установщик Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a461051022791e414fe7e211e4dde33c7e83101b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813841"
---
# <a name="logging-windows-installer"></a><span data-ttu-id="e9abe-103">Ведение журнала (установщик Windows)</span><span class="sxs-lookup"><span data-stu-id="e9abe-103">Logging (Windows Installer)</span></span>

<span data-ttu-id="e9abe-104">Эта [Системная политика](system-policy.md) для компьютера используется, только если ведение журнала не включено с помощью параметра командной строки "/l" или [**мсиенаблелог**](/windows/desktop/api/Msi/nf-msi-msienableloga).</span><span class="sxs-lookup"><span data-stu-id="e9abe-104">This per-machine [system policy](system-policy.md) is used only if logging has not been enabled by the "/L" command line option or by [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga).</span></span> <span data-ttu-id="e9abe-105">Если в этом случае политика задана, установщик создает файл журнала в папке% TEMP% с случайным именем: MSI \* . Журналь.</span><span class="sxs-lookup"><span data-stu-id="e9abe-105">If the policy is set in this case, the installer creates a log file in %temp% with the random name: MSI\*.LOG.</span></span> <span data-ttu-id="e9abe-106">Укажите режим ведения журнала, задав в качестве значения политики строку символов.</span><span class="sxs-lookup"><span data-stu-id="e9abe-106">Specify the logging mode by setting the policy value to a string of characters.</span></span> <span data-ttu-id="e9abe-107">Используйте те же символы, чтобы указать политику режима ведения журнала, используемую [параметром командной строки](command-line-options.md)"/l".</span><span class="sxs-lookup"><span data-stu-id="e9abe-107">Use the same characters to specify logging mode policy as used by the "/L" [command line option](command-line-options.md).</span></span> <span data-ttu-id="e9abe-108">Обратите внимание, что для политики нельзя использовать "+" и " \* ".</span><span class="sxs-lookup"><span data-stu-id="e9abe-108">Note that you cannot use "+" and "\*" for the policy.</span></span>

<span data-ttu-id="e9abe-109">Режим ведения журнала можно задать с помощью политики, параметра командной строки или программно.</span><span class="sxs-lookup"><span data-stu-id="e9abe-109">The logging mode can be set using policy, a command line option, or programmatically.</span></span> <span data-ttu-id="e9abe-110">Дополнительные сведения о всех методах, доступных для настройки режима ведения журнала, см. в разделе " [нормальное ведение журнала](normal-logging.md) " раздела [установщик Windows Logging](windows-installer-logging.md) .</span><span class="sxs-lookup"><span data-stu-id="e9abe-110">For more information about all the methods that are available for setting the logging mode, see [Normal Logging](normal-logging.md) in the [Windows Installer Logging](windows-installer-logging.md) section.</span></span>

<span data-ttu-id="e9abe-111">Можно предотвратить ввод конфиденциальных сведений, например паролей, в файл журнала и сделать их видимыми.</span><span class="sxs-lookup"><span data-stu-id="e9abe-111">You can prevent confidential information, for example passwords, from being entered into the log file and made visible.</span></span> <span data-ttu-id="e9abe-112">Дополнительные сведения см. в разделе [предотвращение записи конфиденциальной информации в файл журнала](preventing-confidential-information-from-being-written-into-the-log-file.md) .</span><span class="sxs-lookup"><span data-stu-id="e9abe-112">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md)</span></span>

## <a name="registry-key"></a><span data-ttu-id="e9abe-113">Ключ реестра</span><span class="sxs-lookup"><span data-stu-id="e9abe-113">Registry Key</span></span>

<span data-ttu-id="e9abe-114">В следующем разделе реестра задайте значение Logging.</span><span class="sxs-lookup"><span data-stu-id="e9abe-114">Set the value named Logging under the following registry key.</span></span>

<span data-ttu-id="e9abe-115">**HKey \_ \_** \\ **Политики программного обеспечения** локального компьютера \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="e9abe-115">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="e9abe-116">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e9abe-116">Data Type</span></span>

<span data-ttu-id="e9abe-117">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="e9abe-117">**REG\_SZ**</span></span>

 

 



