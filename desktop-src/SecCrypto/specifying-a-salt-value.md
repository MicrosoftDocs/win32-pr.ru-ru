---
description: Как базовый, так и расширенный поставщик могут указывать значение и длину расширяющего значения. Базовый поставщик задает расширяющее значение с помощью \_ значения параметра соли. Базовый поставщик всегда задает одиннадцать байтов для расширяющего значения.
ms.assetid: ea56d064-b725-431f-b951-66167624e14b
title: Указание расширяющего значения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9fc8aeea66c536db1c24d7ef3cf4fb9a05b543f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664624"
---
# <a name="specifying-a-salt-value"></a><span data-ttu-id="1b8d5-105">Указание расширяющего значения</span><span class="sxs-lookup"><span data-stu-id="1b8d5-105">Specifying a Salt Value</span></span>

<span data-ttu-id="1b8d5-106">Как базовый, так и расширенный поставщик могут указывать значение и длину [*расширяющего значения*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="1b8d5-106">Both the Base Provider and the Extended Provider can specify the value and length of the [*salt value*](../secgloss/s-gly.md) to be used.</span></span> <span data-ttu-id="1b8d5-107">Базовый поставщик задает расширяющее значение с помощью \_ значения параметра соли.</span><span class="sxs-lookup"><span data-stu-id="1b8d5-107">The Base Provider sets a salt value using the KP\_SALT parameter value.</span></span> <span data-ttu-id="1b8d5-108">Базовый поставщик всегда задает одиннадцать байтов для расширяющего значения.</span><span class="sxs-lookup"><span data-stu-id="1b8d5-108">The Base Provider always sets eleven bytes of salt value.</span></span>

<span data-ttu-id="1b8d5-109">Улучшенный поставщик задает расширяющее значение, вызывая [**криптсеткэйпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) с \_ \_ заданным параметром соли с указанием значения параметра и параметром *pbData* , указывающим на структуру [**\_ \_ больших двоичных объектов с непонятным целым числом**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) , которая содержит Salt-объект.</span><span class="sxs-lookup"><span data-stu-id="1b8d5-109">The Enhanced Provider sets the salt value by calling [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) with the KP\_SALT\_EX parameter value specified and with the *pbData* parameter pointing to a [**CRYPT\_INTEGER\_BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) structure that contains the salt.</span></span>

> [!Note]  
> <span data-ttu-id="1b8d5-110">Общая длина [*симметричного ключа*](../secgloss/s-gly.md) расширенного поставщика и его расширяющего значения не может превышать 128 бит.</span><span class="sxs-lookup"><span data-stu-id="1b8d5-110">The total length of an Enhanced Provider [*symmetric key*](../secgloss/s-gly.md) and its salt value cannot be greater than 128 bits.</span></span>

 

<span data-ttu-id="1b8d5-111">Для \_ обратной совместимости с базовым поставщиком сохраняется соль ключевого значения.</span><span class="sxs-lookup"><span data-stu-id="1b8d5-111">KP\_SALT continues to be provided for backward compatibility with the Base Provider.</span></span> <span data-ttu-id="1b8d5-112">Более новые приложения должны использовать \_ \_ значение параметра ex соли.</span><span class="sxs-lookup"><span data-stu-id="1b8d5-112">Newer applications should use the KP\_SALT\_EX parameter value.</span></span>

<span data-ttu-id="1b8d5-113">В следующем примере задается расширяющее значение.</span><span class="sxs-lookup"><span data-stu-id="1b8d5-113">The following example sets a salt value.</span></span>


```C++
// Specify 4 bytes of salt.
BYTE rgbSalt[] = {0x01, 0x02, 0x03, 0x04};
CRYPT_DATA_BLOB sSaltData;
sSaltData.pbData = rgbSalt;
sSaltData.cbData = sizeof(rgbSalt);

// Set the 4 bytes of salt required.
// hKey is an HCRYPTPROV handle previously
// assigned, such as by CryptImportKey.
if (CryptSetKeyParam(
        hKey,    
        KP_SALT_EX,    
        (BYTE*)&sSaltData,    
        0))
{
     printf("The salt value is set.\n");
}
else
{
     printf("Setting the salt value failed.\n");
}
```



 

 
