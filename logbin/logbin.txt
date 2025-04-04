# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Log-binomial regression Use With (In) R Software
install.packages("logbin")
library("logbin")
logbin = read.csv("https://raw.githubusercontent.com/timbulwidodostp/logbin/main/logbin/logbin.csv",sep = ";")
# Estimation Log-binomial regression Use With (In) R Software
logbin$AgeSev <- 10 * logbin$AgeGroup + logbin$Severity
logbin <- logbin(cbind(Deaths, Patients-Deaths) ~ factor(AgeSev) + factor(Delay) + factor(Region), data = logbin, trace = 1, maxit = 100)
summary(logbin)
# Log-binomial regression Use With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished