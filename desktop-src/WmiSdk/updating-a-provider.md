---
description: Иногда может потребоваться установка более новой версии поставщика на работающую систему.
ms.assetid: 44c4c16a-fd79-483a-81ef-a0f74a2cdf45
ms.tgt_platform: multiple
title: Обновление поставщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4869e6e9f7fbddc3081922f476ca021934065a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693320"
---
# <a name="updating-a-provider"></a><span data-ttu-id="7025c-103">Обновление поставщика</span><span class="sxs-lookup"><span data-stu-id="7025c-103">Updating a Provider</span></span>

<span data-ttu-id="7025c-104">Иногда может потребоваться установка более новой версии поставщика на работающую систему.</span><span class="sxs-lookup"><span data-stu-id="7025c-104">Sometimes you may need to install a newer version of a provider onto a running system.</span></span> <span data-ttu-id="7025c-105">Если поставщик установлен в качестве библиотеки DLL, можно установить новый поставщик, не перезапуская службу, перезагрузить компьютер или иным образом повлиять на приложения, использующие WMI.</span><span class="sxs-lookup"><span data-stu-id="7025c-105">If your provider is installed as a DLL, you can install a new provider without having to restart the service, reboot the computer, or otherwise affect any applications using WMI at that time.</span></span>

<span data-ttu-id="7025c-106">В следующей процедуре описывается обновление поставщика.</span><span class="sxs-lookup"><span data-stu-id="7025c-106">The following procedure describes how to update a provider.</span></span>

<span data-ttu-id="7025c-107">**Обновление поставщика**</span><span class="sxs-lookup"><span data-stu-id="7025c-107">**To update a provider**</span></span>

1.  <span data-ttu-id="7025c-108">Создайте новый поставщик.</span><span class="sxs-lookup"><span data-stu-id="7025c-108">Build the new provider.</span></span>

    1.  <span data-ttu-id="7025c-109">Скомпилируйте новый поставщик с другим именем DLL и другим **идентификатором CLSID**.</span><span class="sxs-lookup"><span data-stu-id="7025c-109">Compile the new provider with a different DLL name and a different **CLSID**.</span></span>

        <span data-ttu-id="7025c-110">Например, измените Myprov.dll на Myprov1.dll, а **CLSID \_ Мипропров** на **CLSID \_ мипров** 1.</span><span class="sxs-lookup"><span data-stu-id="7025c-110">For example, change Myprov.dll to Myprov1.dll, and **CLSID\_MyProProv** to **CLSID\_MyProv** 1.</span></span>

    2.  <span data-ttu-id="7025c-111">Измените MOF-файл регистрации поставщика, чтобы использовать новый CLSID (CLSID \_ MyProv1), но с тем же именем поставщика ("мипров").</span><span class="sxs-lookup"><span data-stu-id="7025c-111">Modify the provider registration MOF file to use the new CLSID (CLSID\_MyProv1), but the same provider name ("MyProv").</span></span>

2.  <span data-ttu-id="7025c-112">Установите новый поставщик.</span><span class="sxs-lookup"><span data-stu-id="7025c-112">Install the new provider.</span></span>

    1.  <span data-ttu-id="7025c-113">Скопируйте новую библиотеку DLL поставщика с новым именем рядом с прежней.</span><span class="sxs-lookup"><span data-stu-id="7025c-113">Copy the new provider DLL with the new name alongside the old one.</span></span>
    2.  <span data-ttu-id="7025c-114">Самостоятельно Зарегистрируйте нового поставщика.</span><span class="sxs-lookup"><span data-stu-id="7025c-114">Self-register the new provider.</span></span>

        <span data-ttu-id="7025c-115">Например, для регистрации нового поставщика используйте команду **regsvr32** **myprov1.dll** .</span><span class="sxs-lookup"><span data-stu-id="7025c-115">For example, use the **regsvr32** **myprov1.dll** command to register the new provider.</span></span>

    3.  <span data-ttu-id="7025c-116">Скомпилируйте новый MOF-файл регистрации поставщика, тем самым перезаписывая старую регистрацию поставщика.</span><span class="sxs-lookup"><span data-stu-id="7025c-116">Compile the new provider registration MOF, thus overwriting the old provider registration.</span></span> <span data-ttu-id="7025c-117">До этой точки старый поставщик был полностью функциональным. Теперь новый поставщик работает полностью.</span><span class="sxs-lookup"><span data-stu-id="7025c-117">Until this point, the old provider was fully functional; now the new provider is fully operational.</span></span>

3.  <span data-ttu-id="7025c-118">При необходимости удалите старую версию поставщика.</span><span class="sxs-lookup"><span data-stu-id="7025c-118">Remove the old version of the provider, if necessary.</span></span>

    1.  <span data-ttu-id="7025c-119">Отмените регистрацию старой библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="7025c-119">Unregister the old DLL.</span></span>

        <span data-ttu-id="7025c-120">Например, чтобы отменить регистрацию старой библиотеки DLL, используйте команду **regsvr32** **/umyprov.dll** .</span><span class="sxs-lookup"><span data-stu-id="7025c-120">For example, use the **regsvr32** **/umyprov.dll** command to unregister the old DLL.</span></span>

    2.  <span data-ttu-id="7025c-121">Пометьте старую библиотеку DLL, которая будет удалена при перезагрузке, вызвав [**мовефиликс**](/windows/desktop/api/winbase/nf-winbase-movefileexa).</span><span class="sxs-lookup"><span data-stu-id="7025c-121">Mark the old DLL to be deleted on reboot by calling [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa).</span></span>

<span data-ttu-id="7025c-122">Для обновления поставщика, реализованного на локальном сервере, можно выполнить аналогичные действия.</span><span class="sxs-lookup"><span data-stu-id="7025c-122">You can take similar steps to upgrade a local server-implemented provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7025c-123">См. также</span><span class="sxs-lookup"><span data-stu-id="7025c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7025c-124">Разработка поставщика WMI</span><span class="sxs-lookup"><span data-stu-id="7025c-124">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="7025c-125">Настройка дескрипторов безопасности Намепаце</span><span class="sxs-lookup"><span data-stu-id="7025c-125">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="7025c-126">Защита поставщика</span><span class="sxs-lookup"><span data-stu-id="7025c-126">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 
