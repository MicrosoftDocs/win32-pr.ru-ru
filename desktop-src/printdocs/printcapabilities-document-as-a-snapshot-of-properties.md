---
title: Документ как моментальный снимок свойств
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 476c98e6-face-42cf-874d-cfa7a54b0666
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d73fc190ed8c259e64fdd60cc291c6ae5b58f80
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104424150"
---
# <a name="printcapabilities-document-as-a-snapshot-of-properties"></a>PrintCapabilities документ в виде моментального снимка свойств

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Устройство, описываемое PrintCapabilities, может иметь свойства, зависящие от состояния или конфигурации устройства. Хотя PrintCapabilities представляет собой полное пространство конфигурации устройства, поставщик PrintCapabilities создает зависящий от конфигурации экземпляр PrintCapabilities, именуемый документом PrintCapabilities. Этот документ PrintCapabilities, зависящий от конфигурации, позволяет избежать появления схемы PrintCapabilities с сложностью представления многозначных данных. Что более важно, чтобы освободить потребителя документа PrintCapabilities от нагрузки из многозначного представления данных, все экземпляры свойств и Скоредпроперти в документе PrintCapabilities должны быть однозначными. Иными словами, каждое свойство и экземпляр Скоредпроперти в документе PrintCapabilities должны иметь фиксированное значение относительно входной конфигурации. Каждый документ PrintCapabilities можно рассматривать как моментальный снимок свойств устройства, когда устройство находится в определенном состоянии. Следовательно, прежде чем можно будет создать документ PrintCapabilities, необходимо указать используемую конфигурацию.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



