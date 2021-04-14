---
description: Удаляет сетевой источник или URL-адрес.
ms.assetid: 76c7cc6c-740f-40e0-8385-024dcc82b79e
title: Метод PATCH. Саурцелистклеарсаурце
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a85afc4eb85a4269284a49809c399dbb65b4894
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651708"
---
# <a name="patchsourcelistclearsource-method"></a>Метод PATCH. Саурцелистклеарсаурце

Метод **саурцелистклеарсаурце** удаляет сеть или источник URL-адреса. Этот метод вызывает [**мсисаурцелистклеарсаурце**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).

## <a name="syntax"></a>Синтаксис


```JScript
Patch.SourceListClearSource(
  Type,
  SourcePath
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Тип* 
</dt> <dd>

Тип удаляемого источника.

<dl><span id="MSISOURCETYPE_NETWORK"></span><span id="msisourcetype_network"></span><dt>

**МСИСАУРЦЕТИПЕ \_ сеть**
</dt><span id="MSISOURCETYPE_URL"></span><span id="msisourcetype_url"></span><dt>

**\_URL-адрес мсисаурцетипе**
</dt> </dl> </dd> <dt>

*SourcePath* 
</dt> <dd>

Путь к удаляемому источнику.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ ипатч определен как 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Защиты**](patch-object.md)
</dt> <dt>

[**мсисаурцелистклеарсаурце**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[Не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




