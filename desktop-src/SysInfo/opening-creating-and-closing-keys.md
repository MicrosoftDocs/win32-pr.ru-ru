---
description: Прежде чем приложение сможет добавлять данные в реестр, оно должно создать или открыть ключ.
ms.assetid: 7b0b24d2-b54f-4243-95d0-2adbd87cb4df
title: Открытие, создание и закрытие ключей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3260c255240ce2c7fb5d13fe28126a1a3f5527
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662542"
---
# <a name="opening-creating-and-closing-keys"></a><span data-ttu-id="eecdc-103">Открытие, создание и закрытие ключей</span><span class="sxs-lookup"><span data-stu-id="eecdc-103">Opening, Creating, and Closing Keys</span></span>

<span data-ttu-id="eecdc-104">Прежде чем приложение сможет добавлять данные в реестр, оно должно создать или открыть ключ.</span><span class="sxs-lookup"><span data-stu-id="eecdc-104">Before an application can add data to the registry, it must create or open a key.</span></span> <span data-ttu-id="eecdc-105">Чтобы создать или открыть ключ, приложение всегда ссылается на ключ в качестве подраздела открытого в данный момент ключа.</span><span class="sxs-lookup"><span data-stu-id="eecdc-105">To create or open a key, an application always refers to the key as a subkey of a currently open key.</span></span> <span data-ttu-id="eecdc-106">Всегда открыты следующие стандартные разделы: **hKey \_ локальный \_ компьютер**, **классы hKey, \_ \_ корень**, **\_ Пользователи hKey** и **hKey \_ текущий \_ пользователь**.</span><span class="sxs-lookup"><span data-stu-id="eecdc-106">The following predefined keys are always open: **HKEY\_LOCAL\_MACHINE**, **HKEY\_CLASSES\_ROOT**, **HKEY\_USERS**, and **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="eecdc-107">Приложение использует функцию [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) , чтобы открыть ключ, и функцию [**регкреатекэйекс**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) для создания ключа.</span><span class="sxs-lookup"><span data-stu-id="eecdc-107">An application uses the [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) function to open a key and the [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) function to create a key.</span></span> <span data-ttu-id="eecdc-108">Дерево реестра может иметь глубину 512 уровней.</span><span class="sxs-lookup"><span data-stu-id="eecdc-108">A registry tree can be 512 levels deep.</span></span> <span data-ttu-id="eecdc-109">С помощью одного вызова API реестра можно создать до 32 уровней за раз.</span><span class="sxs-lookup"><span data-stu-id="eecdc-109">You can create up to 32 levels at a time through a single registry API call.</span></span>

<span data-ttu-id="eecdc-110">Приложение может использовать функцию [**Ошибка RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey) для закрытия ключа и записи содержащихся в реестре данных.</span><span class="sxs-lookup"><span data-stu-id="eecdc-110">An application can use the [**RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey) function to close a key and write the data it contains into the registry.</span></span> <span data-ttu-id="eecdc-111">**Ошибка RegCloseKey** не обязательно записывает данные в реестр перед возвратом; на очистку кэша на жестком диске может потребоваться несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="eecdc-111">**RegCloseKey** does not necessarily write the data to the registry before returning; it can take as much as several seconds for the cache to be flushed to the hard disk.</span></span> <span data-ttu-id="eecdc-112">Если приложение должно явно записать данные реестра на жесткий диск, можно использовать функцию [**функция RegFlushKey вернула**](/windows/desktop/api/Winreg/nf-winreg-regflushkey) .</span><span class="sxs-lookup"><span data-stu-id="eecdc-112">If an application must explicitly write registry data to the hard disk, it can use the [**RegFlushKey**](/windows/desktop/api/Winreg/nf-winreg-regflushkey) function.</span></span> <span data-ttu-id="eecdc-113">Однако **функция RegFlushKey вернула** использует много системных ресурсов и должен вызываться только при крайней необходимости.</span><span class="sxs-lookup"><span data-stu-id="eecdc-113">**RegFlushKey**, however, uses many system resources and should be called only when absolutely necessary.</span></span>

 

 



