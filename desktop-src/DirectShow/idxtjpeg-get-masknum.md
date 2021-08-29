---
description: Метод Get \_ маскнум извлекает код очистки SMPTE.
ms.assetid: 49710d40-acc0-453e-ac9c-882794a0b82d
title: 'Метод Идкстжпег:: get_MaskNum (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_MaskNum
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9265cac204609381e5d3d6d58d4fbd697f623913098e1f9ebe50d891db31b850
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131044"
---
# <a name="idxtjpegget_masknum-method"></a>Метод Идкстжпег:: Get \_ маскнум

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`get_MaskNum`Метод извлекает код очистки SMPTE.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_MaskNum(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Pval* \[ out, retval\]
</dt> <dd>

Получает код очистки SMPTE. Список поддерживаемых SMPTE очистки см. в разделе Переход на [SMPTE очистки](smpte-wipe-transition.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Идкстжпег**](idxtjpeg.md)
</dt> </dl>

 

 




