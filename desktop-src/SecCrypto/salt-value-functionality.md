---
description: Базовый поставщик создает 40-битные симметричные ключи с одиннадцатью байтами расширяющего значения, одиннадцати байтов ненулевой соли, если \_ \_ задано значение шифрования Create соли, или не имеет расширяющего значения.
ms.assetid: f1af0af7-c64e-435a-aef0-7c4ed7bd1199
title: Функция значения соли
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8e3049c431cf909c1008acac26925cd1fa9e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344345"
---
# <a name="salt-value-functionality"></a><span data-ttu-id="275e2-103">Функция значения соли</span><span class="sxs-lookup"><span data-stu-id="275e2-103">Salt Value Functionality</span></span>

<span data-ttu-id="275e2-104">Базовый поставщик создает 40-битные [*симметричные ключи*](../secgloss/s-gly.md) с одиннадцатью байтами [*расширяющего*](../secgloss/s-gly.md)значения, одиннадцати байтов ненулевой соли, если \_ \_ задано значение шифрования Create соли, или не имеет расширяющего значения.</span><span class="sxs-lookup"><span data-stu-id="275e2-104">The Base Provider creates 40-bit [*symmetric keys*](../secgloss/s-gly.md) created with eleven bytes of zero-value [*salt*](../secgloss/s-gly.md), eleven bytes of nonzero salt if CRYPT\_CREATE\_SALT is specified, or no salt value.</span></span> <span data-ttu-id="275e2-105">Однако 40-разрядный симметричный ключ с Salt-значением не эквивалентен 40-разрядному симметричному ключу без Salt.</span><span class="sxs-lookup"><span data-stu-id="275e2-105">A 40-bit symmetric key with zero-value salt, however, is not equivalent to a 40-bit symmetric key without salt.</span></span> <span data-ttu-id="275e2-106">Для взаимодействия ключи должны создаваться без Salt.</span><span class="sxs-lookup"><span data-stu-id="275e2-106">For interoperability, keys must be created without salt.</span></span> <span data-ttu-id="275e2-107">Эта проблема возникает из-за условия по умолчанию, которое выполняется только с ключами ровно 40 бит.</span><span class="sxs-lookup"><span data-stu-id="275e2-107">This problem results from a default condition that occurs only with keys of exactly 40 bits.</span></span> <span data-ttu-id="275e2-108">Все остальные [*длины ключей*](../secgloss/k-gly.md) не имеют расширяющего выделения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="275e2-108">All other [*key lengths*](../secgloss/k-gly.md) do not have salt allocated by default.</span></span>

<span data-ttu-id="275e2-109">Как базовые поставщики, так и расширенный поставщик могут использовать флаг шифрования \_ без \_ помех, чтобы указать, что для 40-разрядного симметричного ключа не выделяется расширяющее значение.</span><span class="sxs-lookup"><span data-stu-id="275e2-109">Both the Base Providers and the Extended Provider can use the CRYPT\_NO\_SALT flag to specify that no salt value is allocated for a 40-bit symmetric key.</span></span> <span data-ttu-id="275e2-110">К функциям, принимающим этот флаг, относятся [**криптженкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey), [**криптдеривекэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)и [**криптимпорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span><span class="sxs-lookup"><span data-stu-id="275e2-110">The functions that accept this flag are [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey), [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey), and [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span></span> <span data-ttu-id="275e2-111">По умолчанию эти функции обеспечивают обратную совместимость для случая с 40-битным симметричным ключом, продолжая использовать расширяющее значение длиной в 11 байтов.</span><span class="sxs-lookup"><span data-stu-id="275e2-111">By default, these functions provide backward compatibility for the 40-bit symmetric key case by continuing the use of the eleven-byte-long zero-value salt.</span></span>

 

 
