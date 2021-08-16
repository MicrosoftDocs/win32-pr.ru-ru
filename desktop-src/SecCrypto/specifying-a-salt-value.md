---
description: Как базовый, так и расширенный поставщик могут указывать значение и длину расширяющего значения. Базовый поставщик задает расширяющее значение с помощью \_ значения параметра соли. Базовый поставщик всегда задает одиннадцать байтов для расширяющего значения.
ms.assetid: ea56d064-b725-431f-b951-66167624e14b
title: Указание расширяющего значения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d80ca64bc69cbcf0ed98d72b5b061616fc3cf641f3970d1533b094ef5687f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897949"
---
# <a name="specifying-a-salt-value"></a>Указание расширяющего значения

Как базовый, так и расширенный поставщик могут указывать значение и длину [*расширяющего значения*](../secgloss/s-gly.md) . Базовый поставщик задает расширяющее значение с помощью \_ значения параметра соли. Базовый поставщик всегда задает одиннадцать байтов для расширяющего значения.

Улучшенный поставщик задает расширяющее значение, вызывая [**криптсеткэйпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) с \_ \_ заданным параметром соли с указанием значения параметра и параметром *pbData* , указывающим на структуру [**\_ \_ больших двоичных объектов с непонятным целым числом**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) , которая содержит Salt-объект.

> [!Note]  
> Общая длина [*симметричного ключа*](../secgloss/s-gly.md) расширенного поставщика и его расширяющего значения не может превышать 128 бит.

 

Для \_ обратной совместимости с базовым поставщиком сохраняется соль ключевого значения. Более новые приложения должны использовать \_ \_ значение параметра ex соли.

В следующем примере задается расширяющее значение.


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



 

 
