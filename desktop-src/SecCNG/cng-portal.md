---
description: CNG — это API шифрования, который можно использовать для создания программного обеспечения безопасности шифрования для управления ключами шифрования, шифрования и защиты данных, а также для шифрования и сетевой безопасности.
ms.assetid: eaad88a1-4e1d-4246-9560-8eef60f8b70f
title: 'API шифрования: следующее поколение'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d485f8371905961c63fbab66b29d0db544e3271
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896642"
---
# <a name="cryptography-api-next-generation"></a><span data-ttu-id="a7c1e-103">API шифрования: следующее поколение</span><span class="sxs-lookup"><span data-stu-id="a7c1e-103">Cryptography API: Next Generation</span></span>

## <a name="purpose"></a><span data-ttu-id="a7c1e-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="a7c1e-104">Purpose</span></span>

<span data-ttu-id="a7c1e-105">API шифрования: следующее поколение (CNG) — это долгосрочная замена интерфейса [*CryptoAPI*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a7c1e-105">Cryptography API: Next Generation (CNG) is the long-term replacement for the [*CryptoAPI*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="a7c1e-106">CNG разработан для расширения на множестве уровней и шифрования, независимо от поведения.</span><span class="sxs-lookup"><span data-stu-id="a7c1e-106">CNG is designed to be extensible at many levels and cryptography agnostic in behavior.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="a7c1e-107">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="a7c1e-107">Developer audience</span></span>

<span data-ttu-id="a7c1e-108">CNG предназначен для использования разработчиками приложений, которые позволяют пользователям создавать и обмениваться документами и другими данными в безопасной среде, особенно на незащищенных носителях, таких как Интернет.</span><span class="sxs-lookup"><span data-stu-id="a7c1e-108">CNG is intended for use by developers of applications that will enable users to create and exchange documents and other data in a secure environment, especially over nonsecure media such as the Internet.</span></span> <span data-ttu-id="a7c1e-109">Разработчики должны быть знакомы с языками программирования C и C++ и средой программирования на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="a7c1e-109">Developers should be familiar with the C and C++ programming languages and the Windows-based programming environment.</span></span> <span data-ttu-id="a7c1e-110">Хотя это и не является обязательным, рекомендуется понимать вопросы, связанные с шифрованием или безопасностью.</span><span class="sxs-lookup"><span data-stu-id="a7c1e-110">Although not required, an understanding of cryptography or security-related subjects is advised.</span></span>

<span data-ttu-id="a7c1e-111">При разработке поставщика алгоритма шифрования CNG или поставщика хранилища ключей необходимо загрузить [пакет средств разработки поставщика служб шифрования](https://www.microsoft.com/download/details.aspx?id=30688) от корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="a7c1e-111">If you are developing a CNG cryptographic algorithm provider or key storage provider, you must download the [Cryptographic Provider Development Kit](https://www.microsoft.com/download/details.aspx?id=30688) from Microsoft.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a7c1e-112">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="a7c1e-112">Run-time requirements</span></span>

<span data-ttu-id="a7c1e-113">CNG поддерживается, начиная с Windows Server 2008 и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a7c1e-113">CNG is supported beginning with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="a7c1e-114">Сведения о требованиях времени выполнения для определенного программного элемента см. в разделе "требования" на странице справочника по этому элементу.</span><span class="sxs-lookup"><span data-stu-id="a7c1e-114">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a7c1e-115">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="a7c1e-115">In this section</span></span>



| <span data-ttu-id="a7c1e-116">Раздел</span><span class="sxs-lookup"><span data-stu-id="a7c1e-116">Topic</span></span>                                         | <span data-ttu-id="a7c1e-117">Описание</span><span class="sxs-lookup"><span data-stu-id="a7c1e-117">Description</span></span>                                                                                                                                    |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a7c1e-118">О CNG</span><span class="sxs-lookup"><span data-stu-id="a7c1e-118">About CNG</span></span>](about-cng.md)<br/>         | <span data-ttu-id="a7c1e-119">Описывает возможности CNG, криптографические примитивы, хранение ключей, извлечение, импорт и экспорт.</span><span class="sxs-lookup"><span data-stu-id="a7c1e-119">Describes CNG features, cryptographic primitives, and key storage, retrieval, import, and export.</span></span><br/>                                   |
| [<span data-ttu-id="a7c1e-120">Использование CNG</span><span class="sxs-lookup"><span data-stu-id="a7c1e-120">Using CNG</span></span>](using-cng.md)<br/>         | <span data-ttu-id="a7c1e-121">Объясняется, как использовать функции настройки шифрования CNG и типичное программирование CNG.</span><span class="sxs-lookup"><span data-stu-id="a7c1e-121">Explains how to use the cryptography configuration features of CNG and typical CNG programming.</span></span><br/>                                     |
| [<span data-ttu-id="a7c1e-122">Справочник по CNG</span><span class="sxs-lookup"><span data-stu-id="a7c1e-122">CNG Reference</span></span>](cng-reference.md)<br/> | <span data-ttu-id="a7c1e-123">Подробное описание элементов программирования CNG.</span><span class="sxs-lookup"><span data-stu-id="a7c1e-123">Detailed descriptions of the CNG programming elements.</span></span> <span data-ttu-id="a7c1e-124">Эти страницы содержат справочные описания API для работы с CNG.</span><span class="sxs-lookup"><span data-stu-id="a7c1e-124">These pages include reference descriptions of the API for working with CNG.</span></span> <br/> |



 

 

