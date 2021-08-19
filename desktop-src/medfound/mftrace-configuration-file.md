---
description: Средство Мфтраце может читать XML-файл конфигурации, указывающий одного или нескольких поставщиков трассировки.
ms.assetid: 70d11a55-041e-4eb5-96a9-238e7ecdd906
title: Файл конфигурации Мфтраце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60969d52405b5aeeb768710d35751d9ea2cab40ca60a7d85a4da1bc1b0c65468
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117871941"
---
# <a name="mftrace-configuration-file"></a>Файл конфигурации Мфтраце

Средство [мфтраце](mftrace.md) может читать XML-файл конфигурации, указывающий одного или нескольких поставщиков трассировки.

Элемент [**providers**](providers.md) является корневым элементом в файле конфигурации.

## <a name="in-this-section"></a>Содержание раздела

-   [**This**](keyword.md)
-   [**мфдетаурс**](mfdetours.md)
-   [**поставщики**](provider.md)
-   [**providers**](providers.md)

## <a name="example"></a>Пример

``` syntax
<?xml version='1.0' encoding='utf-8'?>
<providers>
  <mfdetours level="info"> 
    <keyword ID="MFPlatExport" />
  </mfdetours>
  
  <!-- Manifest-based traces -->

  <provider level="verbose" ID="Microsoft-Windows-MediaFoundation-MFReadWrite">
    <keyword ID="0x0000000000000000" />
  </provider>

</providers>
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[мфтраце](mftrace.md)
</dt> </dl>

 

 



