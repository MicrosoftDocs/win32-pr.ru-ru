---
description: Если для этой системной политики на уровне компьютера задано значение &\# 0034; 1&\# 0034;, установщик предотвращает использование исправлений контроля учетных записей (UAC) для всех приложений, установленных на компьютере, без прав администратора.
ms.assetid: b122d6f4-2be6-4b9b-b8e0-ca08fe9c4f94
title: дисаблелуапатчинг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76357211523d0a69a56ab2a047623a63f211df9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664739"
---
# <a name="disableluapatching"></a><span data-ttu-id="42f43-103">дисаблелуапатчинг</span><span class="sxs-lookup"><span data-stu-id="42f43-103">DisableLUAPatching</span></span>

<span data-ttu-id="42f43-104">Если для этой системной политики на уровне компьютера задано значение "1", установщик не позволяет администраторам использовать [исправление контроля учетных записей (UAC)](user-account-control--uac--patching.md) для любого приложения, установленного на компьютере.</span><span class="sxs-lookup"><span data-stu-id="42f43-104">If this per-machine system policy is set to "1", the installer prevents non-administrators from using [User Account Control (UAC) Patching](user-account-control--uac--patching.md) for any application installed on the computer.</span></span> <span data-ttu-id="42f43-105">Если системная политика на уровне компьютера не задана или имеет значение 0, пользователи, не являющиеся администраторами, могут применять к приложениям, для которых разрешено исправление учетных записей пользователей с минимальными правами доступа, обновления с минимальными правами.</span><span class="sxs-lookup"><span data-stu-id="42f43-105">When the per-machine system policy is not set or set to 0, non-administrators can apply least-privilege user patches to applications that are enabled for least-privilege user account patching.</span></span>

<span data-ttu-id="42f43-106">Используйте свойство [**мсидисаблелуапатчинг**](msidisableluapatching.md) , чтобы предотвратить исправление минимальных прав доступа приложения.</span><span class="sxs-lookup"><span data-stu-id="42f43-106">Use the [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) property to prevent the least-privilege patching of an application.</span></span>

<span data-ttu-id="42f43-107">Политика Дисаблелуапатчинг доступна начиная с версии установщик Windows 3,0.</span><span class="sxs-lookup"><span data-stu-id="42f43-107">The DisableLUAPatching policy is available beginning with Windows Installer version 3.0.</span></span>

## <a name="registry-key"></a><span data-ttu-id="42f43-108">Ключ реестра</span><span class="sxs-lookup"><span data-stu-id="42f43-108">Registry Key</span></span>

<span data-ttu-id="42f43-109">**HKey \_ \_** \\ **Политики программного обеспечения** локального компьютера \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="42f43-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="42f43-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="42f43-110">Data Type</span></span>

<span data-ttu-id="42f43-111">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="42f43-111">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="42f43-112">См. также</span><span class="sxs-lookup"><span data-stu-id="42f43-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42f43-113">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="42f43-113">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



