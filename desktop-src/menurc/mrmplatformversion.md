---
title: Перечисление Мрмплатформверсион (Мрмресаурцеиндексер. h)
description: Определяет константы, указывающие версию платформы. Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки.
ms.assetid: 7BA30B8F-FB23-4DCA-930D-099C7F8476E9
keywords:
- Меню перечисления Мрмплатформверсион и другие ресурсы
topic_type:
- apiref
api_name:
- MrmPlatformVersion
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8127d3e6e99d974315327cf89ae9e82add7bc628
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989298"
---
# <a name="mrmplatformversion-enumeration"></a>Перечисление Мрмплатформверсион

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Определяет константы, указывающие версию платформы. Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _MrmPlatformVersion { 
  MrmPlatformVersion_Default          = 0,
  MrmPlatformVersion_Windows10_0_0_0  = 0x010A0000,
  MrmPlatformVersion_Windows10_0_0_5  = 0x010A0005
} MrmPlatformVersion;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MrmPlatformVersion_Default"></span><span id="mrmplatformversion_default"></span><span id="MRMPLATFORMVERSION_DEFAULT"></span>**Мрмплатформверсион \_ по умолчанию**
</dt> <dd>

Указывает, что версия платформы является версией по умолчанию.

</dd> <dt>

<span id="MrmPlatformVersion_Windows10_0_0_0"></span><span id="mrmplatformversion_windows10_0_0_0"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_0"></span>**Мрмплатформверсион \_ Windows 10 \_ 0 \_ 0 \_**
</dt> <dd>

Указывает версию платформы Windows 10.0.0.0.

</dd> <dt>

<span id="MrmPlatformVersion_Windows10_0_0_5"></span><span id="mrmplatformversion_windows10_0_0_5"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_5"></span>**Мрмплатформверсион \_ Windows 10 \_ 0 \_ 0 \_**
</dt> <dd>

Указывает версию платформы Windows 10.0.0.5.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1803\]<br/>                                       |
| Минимальная версия сервера<br/> | \[Только классические приложения Windows Server\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Мрмресаурцеиндексер. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

