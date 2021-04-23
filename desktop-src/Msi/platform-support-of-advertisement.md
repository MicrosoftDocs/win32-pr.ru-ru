---
description: Установщик Windows поддерживает объявление о приложениях и функциях.
ms.assetid: 9e5158bc-4877-49d1-9bb9-4dd17abb444d
title: Поддержка платформ объявления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48016241998473a5bb5ae8ecff05a14fd702f8be
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105651240"
---
# <a name="platform-support-of-advertisement"></a><span data-ttu-id="4b42f-103">Поддержка платформ объявления</span><span class="sxs-lookup"><span data-stu-id="4b42f-103">Platform Support of Advertisement</span></span>

<span data-ttu-id="4b42f-104">Установщик Windows поддерживает объявление о приложениях и функциях.</span><span class="sxs-lookup"><span data-stu-id="4b42f-104">The Windows Installer supports advertisement of applications and features.</span></span>

<span data-ttu-id="4b42f-105">Следующие возможности объявления доступны в Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="4b42f-105">The following advertisement capabilities are available on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP, and Windows 2000.</span></span>

-   <span data-ttu-id="4b42f-106">Ярлыки и их значки.</span><span class="sxs-lookup"><span data-stu-id="4b42f-106">Shortcuts and their icons.</span></span>

-   <span data-ttu-id="4b42f-107">Расширения и их значки, указанные в [таблице ProgID](progid-table.md).</span><span class="sxs-lookup"><span data-stu-id="4b42f-107">Extensions and their icons specified in the [ProgId Table](progid-table.md).</span></span>

-   <span data-ttu-id="4b42f-108">Команды оболочки и команд, зарегистрированные под ключом ProgId.</span><span class="sxs-lookup"><span data-stu-id="4b42f-108">Shell and command Verbs registered underneath the ProgId key.</span></span>

-   <span data-ttu-id="4b42f-109">Контексты CLSID и Инпрочандлер.</span><span class="sxs-lookup"><span data-stu-id="4b42f-109">CLSID contexts and InProcHandler.</span></span>

-   <span data-ttu-id="4b42f-110">Install-On-Demand by OLE доступен только программно с помощью [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) (C/C++) и **функции CreateObject (Visual Basic)** или **функции GetObject (Visual Basic)**.</span><span class="sxs-lookup"><span data-stu-id="4b42f-110">Install-On-Demand through OLE is only available programmatically through [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) (C/C++), and **CreateObject Function (Visual Basic)** or **GetObject Function (Visual Basic)**.</span></span>

> [!Note]
> <span data-ttu-id="4b42f-111">Сведения AppId и typelib записываются только при установке объявленного компонента.</span><span class="sxs-lookup"><span data-stu-id="4b42f-111">AppId and Typelib information is only written when an advertised component is installed.</span></span>
> 
> <span data-ttu-id="4b42f-112">Для поддержки расширений имен файлов приложение должно быть опубликовано для Active Directory администратором с помощью групповая политика.</span><span class="sxs-lookup"><span data-stu-id="4b42f-112">To support file name extensions, the application must be published to Active Directory by an administrator using Group Policy.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b42f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b42f-113">Remarks</span></span>

<span data-ttu-id="4b42f-114">Установка продукта может не требовать перезагрузки, но все объявленные сочетания клавиш не будут работать, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="4b42f-114">The installation of the product may not require a restart, but any advertised shortcuts do not work until the machine is restarted.</span></span> <span data-ttu-id="4b42f-115">Объявленные сочетания клавиш для последующих установок работают без перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="4b42f-115">The advertised shortcuts of subsequent installations work without a restart.</span></span>

<span data-ttu-id="4b42f-116">Чтобы обеспечить правильную работу объявленных сочетаний клавиш, автор пакета должен запланировать принудительную перезагрузку в конце установки.</span><span class="sxs-lookup"><span data-stu-id="4b42f-116">To ensure that advertised shortcuts work correctly, the package author should schedule a forced restart at the end of the installation.</span></span>

<span data-ttu-id="4b42f-117">Чтобы избежать ненужных перезагрузок системы, запланируйте перезапуск, чтобы запустить его только в том случае, если не установлена ни одна версия установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="4b42f-117">To avoid unnecessary restarts of the system, schedule a restart to run only if no version of the Windows Installer is installed.</span></span>

<span data-ttu-id="4b42f-118">Условные операторы могут проверять свойство [**шелладвтсуппорт**](shelladvtsupport.md) и свойство [**Version9X**](version9x.md) .</span><span class="sxs-lookup"><span data-stu-id="4b42f-118">Conditional statements can check the [**ShellAdvtSupport**](shelladvtsupport.md) property and [**Version9X**](version9x.md) property.</span></span> <span data-ttu-id="4b42f-119">Дополнительные сведения о планировании условных перезапусков см. в разделе [Перезагрузка системы](system-reboots.md) и [использование свойств в условных инструкциях](using-properties-in-conditional-statements.md).</span><span class="sxs-lookup"><span data-stu-id="4b42f-119">For more information about scheduling a conditional forced restarts, see [System Reboots](system-reboots.md) and [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md).</span></span>

 

 
