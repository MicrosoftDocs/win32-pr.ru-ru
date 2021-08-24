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
ms.openlocfilehash: c41eec2f3839de5a8de6bcfd2f3a12910d146a0c2327286024ba36a52526d0a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662984"
---
# <a name="mrmplatformversion-enumeration"></a>Перечисление Мрмплатформверсион

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

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

указывает версию платформы Windows 10.0.0.0.

</dd> <dt>

<span id="MrmPlatformVersion_Windows10_0_0_5"></span><span id="mrmplatformversion_windows10_0_0_5"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_5"></span>**Мрмплатформверсион \_ Windows 10 \_ 0 \_ 0 \_**
</dt> <dd>

указывает версию платформы Windows 10.0.0.5.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1803\]<br/>                                       |
| Минимальная версия сервера<br/> | Windows Только серверные \[ классические приложения\]<br/>                                                 |
| Заголовок<br/>                   | <dl> <dt>Мрмресаурцеиндексер. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

