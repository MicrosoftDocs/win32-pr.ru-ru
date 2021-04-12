---
description: Непрозрачные BLOB-объекты, также известные как Опакуекэйблобс, используются для хранения ключей сеанса в формате, зависящем от поставщика, например SChannel.
ms.assetid: a0756c03-0c27-41ff-9b74-8af462e09675
title: Непрозрачный тип большого двоичного объекта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e45cf8899d5cc63fb360a6b5e4177733de3880f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424037"
---
# <a name="opaque-blob-type"></a><span data-ttu-id="0665c-103">Непрозрачный тип большого двоичного объекта</span><span class="sxs-lookup"><span data-stu-id="0665c-103">Opaque BLOB Type</span></span>

<span data-ttu-id="0665c-104">[*Непрозрачные BLOB-объекты*](../secgloss/o-gly.md), также известные как опакуекэйблобс, используются для хранения [*ключей сеанса*](../secgloss/s-gly.md) в формате, зависящем от поставщика, например [*SChannel*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0665c-104">[*Opaque BLOBs*](../secgloss/o-gly.md), also known as OPAQUEKEYBLOBs, are used to store [*session keys*](../secgloss/s-gly.md) in a vendor-specific format, such as [*Schannel*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="0665c-105">Они содержат базовый материал ключа и все сведения о текущем [*состоянии*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="0665c-105">They contain the base key material and all current [*state*](../secgloss/s-gly.md) information.</span></span> <span data-ttu-id="0665c-106">Сюда входят такие сведения, как [*расширяющее значение*](../secgloss/s-gly.md), [*вектор инициализации*](../secgloss/i-gly.md)и таблица ключей.</span><span class="sxs-lookup"><span data-stu-id="0665c-106">This includes information such as the [*salt value*](../secgloss/s-gly.md), the [*initialization vector*](../secgloss/i-gly.md), and the key table.</span></span> <span data-ttu-id="0665c-107">Формат непрозрачных больших двоичных объектов не опубликован.</span><span class="sxs-lookup"><span data-stu-id="0665c-107">The format of opaque BLOBs is unpublished.</span></span> <span data-ttu-id="0665c-108">Каждый поставщик CSP определяет собственный формат больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="0665c-108">Each CSP vendor determines its own BLOB format.</span></span>

<span data-ttu-id="0665c-109">Поскольку ключ экспортируется в непрозрачный большой двоичный объект в формате, характерном для CSP, он может быть импортирован только в CSP, из которого он был изначально экспортирован.</span><span class="sxs-lookup"><span data-stu-id="0665c-109">Because a key is exported into an opaque BLOB in CSP-specific format, it can only be imported into the CSP from which it was originally exported.</span></span>

<span data-ttu-id="0665c-110">Когда участвуют два процесса, каждый [*процесс*](../secgloss/p-gly.md) вызывает [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) отдельно.</span><span class="sxs-lookup"><span data-stu-id="0665c-110">When two processes are involved, each [*process*](../secgloss/p-gly.md) calls [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) independently.</span></span> <span data-ttu-id="0665c-111">Каждый процесс получает маркер контейнера ключей.</span><span class="sxs-lookup"><span data-stu-id="0665c-111">Each process gets a handle to a key container.</span></span> <span data-ttu-id="0665c-112">Оба процесса могут иметь дескрипторы одного и того же контейнера ключей.</span><span class="sxs-lookup"><span data-stu-id="0665c-112">It is possible for both processes to have handles to the same key container.</span></span> <span data-ttu-id="0665c-113">Один процесс создает ключи и экспортирует их в непрозрачные BLOB-объекты, а затем передает большие двоичные объекты второму процессу.</span><span class="sxs-lookup"><span data-stu-id="0665c-113">One process creates the keys and exports them into opaque BLOBs, then passes the BLOBs to the second process.</span></span> <span data-ttu-id="0665c-114">Второй процесс импортирует ключи из большого двоичного объекта в [*контейнер ключей*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0665c-114">The second process imports the keys from the BLOB into its [*key container*](../secgloss/k-gly.md).</span></span>

<span data-ttu-id="0665c-115">Если CSP оборудования не поддерживает экспорт ключей, большой двоичный объект может содержать только индекс регистра ключа или что-то подобное.</span><span class="sxs-lookup"><span data-stu-id="0665c-115">If a hardware CSP does not support exporting keys, the BLOB might only contain the index of a key register, or something similar.</span></span> <span data-ttu-id="0665c-116">В этом случае оставшаяся часть процедуры игнорируется.</span><span class="sxs-lookup"><span data-stu-id="0665c-116">In this case, the rest of the procedure is ignored.</span></span>

``` syntax
<secure process>
cbBlob = sizeof(rgbBlob);
CryptExportKey(
          hKey, 
          0, 
          OPAQUEKEYBLOB, 
          0, 
          rgbBlob, 
          &cbBlob);
hKey = 0;

<BLOB is transferred to other process>

<user process>
CryptImportKey(
            hProv, 
            pbBlob, 
            cbBlob, 
            0, 
            0, 
            &hKey);
```

 

 
