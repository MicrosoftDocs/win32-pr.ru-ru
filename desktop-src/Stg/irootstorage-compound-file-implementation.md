---
title: Ирутстораже — реализация составного файла
description: Реализация Ирутстораже для составных файлов COM позволяет сохранять файлы в ситуациях нехватки памяти или нехватке места на диске. Сведения о работе этого интерфейса см. в разделе Ирутстораже.
ms.assetid: 0847929e-63ce-42f9-9d47-2e7222e003bb
keywords:
- Ирутстораже Стрктд STG, реализация составного файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928f78e88ffaa526006c0a33e803076db0ec301e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780105"
---
# <a name="irootstorage---compound-file-implementation"></a><span data-ttu-id="e45c5-105">Ирутстораже — реализация составного файла</span><span class="sxs-lookup"><span data-stu-id="e45c5-105">IRootStorage - Compound File Implementation</span></span>

<span data-ttu-id="e45c5-106">Реализация [**ирутстораже**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) для составных файлов com позволяет сохранять файлы в ситуациях нехватки памяти или нехватке места на диске.</span><span class="sxs-lookup"><span data-stu-id="e45c5-106">COM's compound file implementation of [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) allows you to support saving files in low-memory or low disk-space situations.</span></span> <span data-ttu-id="e45c5-107">Сведения о работе этого интерфейса см. в разделе **ирутстораже**.</span><span class="sxs-lookup"><span data-stu-id="e45c5-107">For information on how this interface behaves, see **IRootStorage**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="e45c5-108">Назначение</span><span class="sxs-lookup"><span data-stu-id="e45c5-108">When to Use</span></span>

<span data-ttu-id="e45c5-109">Используйте предоставляемую системой реализацию [**ирутстораже**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) только для поддержки сохранения файлов в условиях нехватки памяти.</span><span class="sxs-lookup"><span data-stu-id="e45c5-109">Use the system-supplied implementation of [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) only to support saving files under low-memory conditions.</span></span>

## <a name="remarks"></a><span data-ttu-id="e45c5-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e45c5-110">Remarks</span></span>

<span data-ttu-id="e45c5-111">Для выполнения обычной операции сохранения в другом файле можно вызвать реализацию [**ирутстораже:: свитчтофиле**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile) в com.</span><span class="sxs-lookup"><span data-stu-id="e45c5-111">It is possible to call COM's implementation of [**IRootStorage::SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile) to do a normal save-as operation to another file.</span></span> <span data-ttu-id="e45c5-112">Однако приложения, которые это делают, могут быть несовместимы с будущими поколениями хранилища COM.</span><span class="sxs-lookup"><span data-stu-id="e45c5-112">However, applications that do this might not be compatible with future generations of COM storage.</span></span> <span data-ttu-id="e45c5-113">Чтобы избежать этой ситуации, приложения, выполняющие операцию "Сохранить как", должны вручную создать второй составной файл и вызвать метод [**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto).</span><span class="sxs-lookup"><span data-stu-id="e45c5-113">To avoid this possibility, applications performing a save-as operation should manually create the second compound file and invoke [**IStorage::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto).</span></span> <span data-ttu-id="e45c5-114">Метод **ирутстораже:: свитчтофиле** следует использовать только в экстренных ситуациях (нехватка памяти или дискового пространства).</span><span class="sxs-lookup"><span data-stu-id="e45c5-114">The **IRootStorage::SwitchToFile** method should be used only in emergency (low-memory or disk-space) situations.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e45c5-115">См. также</span><span class="sxs-lookup"><span data-stu-id="e45c5-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e45c5-116">**ирутстораже**</span><span class="sxs-lookup"><span data-stu-id="e45c5-116">**IRootStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[<span data-ttu-id="e45c5-117">**Ирутстораже:: Свитчтофиле**</span><span class="sxs-lookup"><span data-stu-id="e45c5-117">**IRootStorage::SwitchToFile**</span></span>](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile)
</dt> </dl>

 

 




