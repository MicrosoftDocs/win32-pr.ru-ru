---
description: Метод Жетмаксимумкурсорс извлекает максимальное число курсоров, поддерживаемое планшетным устройством.
ms.assetid: 5a43d792-e64c-4506-9792-31efe0885959
title: 'Метод ITablet3:: Жетмаксимумкурсорс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.GetMaximumCursors
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 7c40184d35ac1d42cb5f5e845396b40efc2d928e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719562"
---
# <a name="itablet3getmaximumcursors-method"></a>Метод ITablet3:: Жетмаксимумкурсорс

Метод **жетмаксимумкурсорс** извлекает максимальное число курсоров, поддерживаемое планшетным устройством.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetMaximumCursors(
   ULONG *pMaximumCursors
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмаксимумкурсорс* 
</dt> <dd>

Максимальное число входов, поддерживаемое устройством.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК в случае успеха; в противном случае возвращает код ошибки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                             |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                |
| Библиотека<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ITablet3**](itablet3.md)
</dt> </dl>

 

 




