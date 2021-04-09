---
description: Разработчики могут предотвратить ввод конфиденциальных сведений, например паролей, в файл журнала во время установки установщик Windows.
ms.assetid: 950c3c56-3f16-4e1a-875f-d31f45065076
title: Предотвращение записи конфиденциальной информации в файл журнала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17880f18ca08745ab1f4f764397e17b7af8827e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080668"
---
# <a name="preventing-confidential-information-from-being-written-into-the-log-file"></a><span data-ttu-id="e6416-103">Предотвращение записи конфиденциальной информации в файл журнала</span><span class="sxs-lookup"><span data-stu-id="e6416-103">Preventing Confidential Information from Being Written into the Log File</span></span>

<span data-ttu-id="e6416-104">При использовании установщик Windows можно предотвратить ввод конфиденциальных сведений, например паролей, в файл журнала и сделать видимыми.</span><span class="sxs-lookup"><span data-stu-id="e6416-104">When using the Windows Installer, you can prevent confidential information, for example passwords, from being entered into the log file and made visible.</span></span>

-   <span data-ttu-id="e6416-105">Установщик никогда не записывает сведения в столбец password [таблицы сервицеинсталл](serviceinstall-table.md) в журнал.</span><span class="sxs-lookup"><span data-stu-id="e6416-105">The Installer never writes the information in the Password column of the [ServiceInstall table](serviceinstall-table.md) into the log.</span></span>
-   <span data-ttu-id="e6416-106">Можно запретить установщику записывать свойство, связанное с [элементом управления](edit-control.md) "поле ввода", в журнал, установив [атрибут элемента управления Password](password-control-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="e6416-106">You can prevent the Installer from writing the property that is associated with an [Edit Control](edit-control.md) into the log by setting the [Password Control Attribute](password-control-attribute.md).</span></span> <span data-ttu-id="e6416-107">Свойство, связанное с элементом управления "поле ввода", имеющим атрибут элемента управления "пароль", скрывается, даже если для политики [отладки](debug.md) задано значение 7.</span><span class="sxs-lookup"><span data-stu-id="e6416-107">The property associated with an Edit Control that has the Password Control Attribute is hidden even if the [Debug](debug.md) policy is set to a value of 7.</span></span>
-   <span data-ttu-id="e6416-108">Можно запретить установщику записывать закрытое свойство в журнал, включив свойство в свойство [**мсихидденпропертиес**](msihiddenproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="e6416-108">You can prevent the Installer from writing a private property into the log by including the property in the [**MsiHiddenProperties**](msihiddenproperties.md) property.</span></span>
    > [!Note]  
    > <span data-ttu-id="e6416-109">Этот метод может сделать так, чтобы конфиденциальные сведения были указаны в командной строке, видимой в журнале.</span><span class="sxs-lookup"><span data-stu-id="e6416-109">This method can make confidential information entered on a command line visible in the log.</span></span> <span data-ttu-id="e6416-110">Если для политики [отладки](debug.md) задано значение 7, установщик будет записывать в журнал сведения, указанные в командной строке.</span><span class="sxs-lookup"><span data-stu-id="e6416-110">When the [Debug](debug.md) policy is set to a value of 7, the installer will write information entered on a command line into the log.</span></span> <span data-ttu-id="e6416-111">Это делает свойство, введенное в командную строку, видимым даже в том случае, если свойство включено в свойство [**мсихидденпропертиес**](msihiddenproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="e6416-111">This makes the property entered on a command line visible even if the property is included in the [**MsiHiddenProperties**](msihiddenproperties.md) property.</span></span>

     

-   <span data-ttu-id="e6416-112">Можно предотвратить запись данных из целевого столбца таблицы [CustomAction](customaction-table.md) в журнал, включив флаг хидетаржет bit в поле Type таблицы CustomAction.</span><span class="sxs-lookup"><span data-stu-id="e6416-112">You can prevent the information in the Target column of the [CustomAction](customaction-table.md) Table from being written into the log by including the HideTarget bit flag in the Type field of the CustomAction table.</span></span> <span data-ttu-id="e6416-113">Значение этого флага равно 8192 (0x2000).</span><span class="sxs-lookup"><span data-stu-id="e6416-113">The value of this flag is 8192 (0x2000).</span></span> <span data-ttu-id="e6416-114">Дополнительные сведения см. в статье [параметр скрытого целевого объекта настраиваемого действия](custom-action-hidden-target-option.md).</span><span class="sxs-lookup"><span data-stu-id="e6416-114">For more information, see [Custom Action Hidden Target Option](custom-action-hidden-target-option.md).</span></span>

 

 



