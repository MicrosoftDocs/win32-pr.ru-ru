---
title: Параметры создания пула плиток
description: Параметры в этом разделе используются для определения пулов плиток с помощью API CreateBuffer ID3D11Device.
ms.assetid: 04290AAF-8517-4557-954E-1CAA3A0CA7F6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7350dc01c845542b97674189a120c0d55db95c282dc80b11fda66230618f99b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119480"
---
# <a name="tile-pool-creation-parameters"></a>Параметры создания пула плиток

Параметры в этом разделе используются для определения пулов плиток с помощью API [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) .

<dl> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Изменять**
</dt> <dd>

Размер выделения, кратный 64 КБ. 0 является допустимым, так как позднее вы можете использовать операцию [**ID3D11DeviceContext2:: ресизетилепул**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) .

</dd> <dt>

<span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Поддерживаемые флаги для ресурсов**
</dt> <dd>

D3D11 \_ \_ \_ пул плиток ресурсов \_ (определяет ресурс как пул плиток), \_ \_ Общие ресурсы, общие \_ \_ \_ кэйедмутекс или \_ Общие \_ нсандле для ресурса D3D11.

</dd> <dt>

<span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Поддерживаемое использование ресурсов**
</dt> <dd>

D3D11 \_ использование \_ только по умолчанию.

</dd> </dl>

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание мозаичных ресурсов](creating-tiled-resources.md)
</dt> </dl>

 

 




